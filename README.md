## LIvES NLP Team presentation at the Society of Behavioral Medicine (2022)

**Details**

- Presentation type:
  - Poster Presentation
- Title:
  - Lessons Learned from a Secondary Analysis Using Natural Language Processing and Machine Learning from a Lifestyle Intervention
- Session date and place:
  - Friday, April 8 from 5:00 PM to 5:50 PM at the Hilton Baltimore Inner Harbor
- Poster available at:
  - ![LIvES SBM 2022 Poster](https://docs.google.com/presentation/d/1HuWLNhYB-IOflkUaE5d84KNCFW-QXl2ATyTQV5lwu8U/edit?usp=sharing)
- Corresponding authors:
  - Dr. Steven J. Bethard (bethard@arizona.edu)
  - Dr. Tracy E. Crane (tecrane@med.miami.edu)


**Cite as**

Sarah Freylersythe, Rebecca Sharp, John Culnan, Damian Yukio Romero Diaz, Yiyun Zhao, G. Hagan Franks, Remo Nitschke, Steven J. Bethard, and Tracy E. Crane. 2022. Lessons Learned from a Secondary Analysis Using Natural Language Processing and Machine Learning from a Lifestyle Intervention: SBM Conference Handout. Retrieved from https://github.com/clulab/SBM_2022_LIvES

*Note: This citation is in [ACM format](https://www.acm.org/publications/authors/reference-formatting). For other formatting please use the "`Cite this repository`" button on the right menu of this repository along with a bibtext converter such as this one: [Online Bibtex Converter](https://asouqi.github.io/bibtex-converter/)*


**License**

The content of this repository is distributed freely under a Creative Commons 4.0 International license (CC by 4.0). You are free to share and adapt as long as you use the citation below, provide a link to the license, and indicate if changes were made. The full license can be found at [https://creativecommons.org/licenses/by/4.0/legalcode](https://creativecommons.org/licenses/by/4.0/legalcode).

![CC by 4.0 logo](https://i.creativecommons.org/l/by/4.0/88x31.png)


# Lessons Learned from a Secondary Analysis Using Natural Language Processing and Machine Learning from a Lifestyle Intervention


## SBM Conference Handout


![Iceberg figure](https://github.com/clulab/SBM_2022_LIvES/blob/main/visuals/iceberg_figure.png)


## Background

Recorded telephone coaching sessions (approximately 24,500) in English and Spanish from 1205 women participating in the Lifestyle Intervention for oVarian cancer Enhanced Survival (LIvES), GOG 0225, study were used for this analysis. The LIvES Study tested whether a lifestyle intervention of increased physical activity and a healthy diet would increase progression-free survival compared to an attention control using trained health coaches and Motivational Interviewing (MI), a directive, patient-centered counseling approach; 323 LIvES Study coaching session recordings were scored for adherence to MI techniques. Here we describe lessons learned from a secondary analysis of LIvES data utilizing machine learning and natural language processing to automate fidelity and predict lifestyle behavioral outcomes.
### Issues

Numerous steps were necessary to prepare the call recordings for natural language processing. Data were aligned through a combination of participant phone numbers, coach names and participant names, entry dates and recording dates. Transcription was performed automatically with wav2vec. An annotation interface was developed using Label Studio and an annotation guideline was adapted from existing Motivational Interviewing Treatment Integrity (MITI) 3.0. Finally, a pilot annotation of the call recordings was completed and initial inter-rater reliability was measured.

### Lessons learned

The process of preparing this secondary analysis resulted in a number of lessons learned. First, data infrastructure for the original LIvES study, due to its long-running nature, evolved in ways that lost data continuity. The data alignment process would have been simplified by establishing a single identifier to link calls, outcomes, and MITI scores, and maintaining that identifier over the course of the project. Second, evaluating the quality of automated transcription systems is difficult and could have been streamlined by manually transcribing a small number of study calls to be used for evaluation. Finally, training a machine learning model to assess interviewer turns could have been simplified by establishing a protocol for coding MITI scoring using an annotation tool, resulting in turn-level annotations alongside the holistic scoring typical of MITI.

### Conclusion

Behavioral interventions should engage the support of a computational scientist in the study design planning stage to take advantage of the largely under-utilized data collected in these trials.

### Acknowledgement of financial support

This work was supported by the following grants:

- LIvES Study (GOG 0225) NCT00719303
- BMISR UACC P30 CA023074
- NLP/ML NIH/NCI 1R21CA256680-01


 MPIs:
 - Dr. Steven J. Bethard
 - Dr. Tracy E. Crane

### References

Damian Yukio Romero Diaz. (2022). "Using natural language processing to determine predictors of healthy diet and physical activity behavior change in ovarian cancer survivors" [Data Management Plan]. DMPHub. https://doi.org/10.48321/D1BK5T

Alejandra Irlena Peñaloza. (2020). Responsiveness to Motivational Interviewing Among Latina Ovarian Cancer Survivors Participating in a Large, Well Powered RCT: A Mixed Methods Analysis [University of Arizona]. UA Campus Repository. http://hdl.handle.net/10150/642195

Cynthia A. Thomson, Tracy E. Crane, Austin Miller, David O. Garcia, Karen Basen-Engquist, David S. Alberts (2016). A randomized trial of diet and physical activity in women treated for stage II–IV ovarian cancer: Rationale and design of the Lifestyle Intervention for Ovarian Cancer Enhanced Survival (LIVES): An NRG Oncology/Gynecologic Oncology Group (GOG-225) Study. Contemporary Clinical Trials, 49, 181–189. https://doi.org/10.1016/j.cct.2016.07.005


https://clinicaltrials.gov/ct2/show/NCT00719303