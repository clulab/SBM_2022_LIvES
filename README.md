## LIvES NLP Team presentation at the Society of Behavioral Medicine (2022)

**Poster Presentation**

Lessons Learned from a Secondary Analysis Using Natural Language Processing and Machine Learning from a Lifestyle Intervention

**Session date**

Friday, April 8 from 5:00 PM to 5:50 PM at the Hilton Baltimore Inner Harbor

Poster [link](https://docs.google.com/presentation/d/1HuWLNhYB-IOflkUaE5d84KNCFW-QXl2ATyTQV5lwu8U/edit?usp=sharing)

### Authors

Sarah Freylersythe(1), Rebecca Sharp(7),  John Culnan(5), Damian Y. Romero Diaz(3), Yiyun Zhao (5), G. Hagan Franks(6),  Remo Nitschke(5), Steven J. Bethard(2), Tracy E. Crane(4)

1. University of Arizona Cancer Center, Tucson, AZ
2. School of Information, College of Social and Behavioral Sciences, University of Arizona, Tucson, AZ
3. Department of Spanish and Portuguese, College of Humanities, University of Arizona, Tucson, AZ
4. Sylvester Comprehensive Cancer Center, University of Miami, Miami, FL
5. Department of Linguistics, College of Social and Behavioral Sciences, University of Arizona, Tucson, AZ
6. Data Science Institute, University of Arizona, Tucson, AZ
7. Lex Machina, Menlo Park, CA


### Abstract
 
**Background**: Recorded telephone coaching sessions (approximately 24,500) in English and Spanish from 1205 women participating in the Lifestyle Intervention for oVarian cancer Enhanced Survival (LIvES), GOG 0225, study were used for this analysis. The LIvES Study tested whether a lifestyle intervention of increased physical activity and a healthy diet would increase progression-free survival compared to an attention control using trained health coaches and Motivational Interviewing (MI), a directive, patient-centered counseling approach; 323 LIvES Study coaching session recordings were scored for adherence to MI techniques. Here we describe lessons learned from a secondary analysis of LIvES data utilizing machine learning and natural language processing to automate fidelity and predict lifestyle behavioral outcomes.

**Methods**: Numerous steps were necessary to prepare the call recordings for natural language processing. Data were aligned through a combination of participant phone numbers, coach names and participant names, entry dates and recording dates. Transcription was performed automatically with wav2vec. An annotation interface was developed using Label Studio and an annotation guideline was adapted from existing Motivational Interviewing Treatment Integrity (MITI) 3.0. Finally, a pilot annotation of the call recordings was completed and initial inter-rater reliability was measured.

**Results**: The process of preparing this secondary analysis resulted in a number of lessons learned. First, data infrastructure for the original LIvES study, due to its long-running nature, evolved in ways that lost data continuity. The data alignment process would have been simplified by establishing a single identifier to link calls, outcomes, and MITI scores, and maintaining that identifier over the course of the project. Second, evaluating the quality of automated transcription systems is difficult and could have been streamlined by manually transcribing a small number of study calls to be used for evaluation. Finally, training a machine learning model to assess interviewer turns could have been simplified by establishing a protocol for coding MITI scoring using an annotation tool, resulting in turn-level annotations alongside the holistic scoring typical of MITI.

**Conclusion**: Behavioral interventions should engage the support of a computational scientist in the study design planning stage to take advantage of the largely under-utilized data collected in these trials.
