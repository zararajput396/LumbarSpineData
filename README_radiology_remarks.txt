LumbarSpineData – radiology remarks and diagnostic labels
=========================================================

File: LumbarSpineData_radiology_remarks.csv (UTF-8, comma-separated, 459 rows, one per patient)

Columns
  public_id                  Patient identifier (LS_000001 ... ). Matches the identifiers of the MRI images
                             in this dataset.
  radiology_remark           The radiologist's remark for the patient's MRI examination. Line breaks in the
                             original remarks were replaced by single spaces; the wording is otherwise unchanged.
  diagnostic_labels          The patient's diagnostic categories as text, separated by semicolons.
  Normal_Spine ... Tumor_Postoperative_Change
                             One column per diagnostic category (1 = present, 0 = absent):
                               Normal_Spine                                Normal Spine
                               Diffuse_Disc_Bulge                          Diffuse Disc Bulge
                               Disc_Bulge                                  Disc Bulge
                               Disc_Protrusion                             Disc Protrusion
                               Spinal_Canal_Stenosis                       Spinal Canal Stenosis
                               Disc_Degeneration                           Disc Degeneration
                               Spinal_Alignment_Structural_Abnormalities   Spinal Alignment and Structural Abnormalities
                               Vertebral_Endplate_Pathologies              Vertebral and Endplate Pathologies
                               Infectious_Inflammatory_Lesions             Infectious and Inflammatory Lesions
                               Tumor_Postoperative_Change                  Tumor and Postoperative Change
  number_of_positive_labels  Number of diagnostic categories present for the patient (all ten categories).
  in_five_label_study        1 if the patient is in the 435-patient cohort of the accompanying five-label study
                             (patients with at least one of the first five categories), otherwise 0.

Patients per category: Normal Spine 57, Diffuse Disc Bulge 185, Disc Bulge 117, Disc Protrusion 118,
Spinal Canal Stenosis 68, Disc Degeneration 23, Spinal Alignment and Structural Abnormalities 15,
Vertebral and Endplate Pathologies 15, Infectious and Inflammatory Lesions 10, Tumor and Postoperative Change 8.
Categories per patient: one 312, two 137, three 10.

Provenance and notes
- Remarks and labels were provided by the reporting radiologist from the same reading of each examination.
- For the 435 patients in the five-label study, the remark is exactly the text used as model input in that study.
- Category names were standardized in capitalization only ("Disc bulge" and "Disc protrusion" are written as
  "Disc Bulge" and "Disc Protrusion").
- Labels record the diagnostic categories assigned by the radiologist. Remarks can also mention findings that were
  not assigned as separate categories, such as canal stenosis described as the consequence of a disc lesion, or
  findings at other disc levels. Labels and remarks are therefore related but not equivalent.
- Normal_Spine indicates that the patient had no finding in any of the other nine categories; it never co-occurs
  with another category.
- The remarks contain no patient names, ages, dates, hospital identifiers, or other direct identifiers.
