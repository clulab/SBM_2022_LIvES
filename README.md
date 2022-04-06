## LIvES NLP Team presentation at the Society of Behavioral Medicine (2022)

![visitors](https://visitor-badge.glitch.me/badge?page_id=damian-romero/clulab/SBM_2022_LIvES&left_color=green&right_color=red)
### Details

- **Presentation type:**
  - Poster Presentation
- **Title:**
  - Lessons Learned from a Secondary Analysis Using Natural Language Processing and Machine Learning from a Lifestyle Intervention
- **Session date and place:**
  - Friday, April 8, from 5:00 PM to 5:50 PM at the Hilton Baltimore Inner Harbor
- **Poster available at:**
  - [LIvES SBM 2022 Poster](https://docs.google.com/presentation/d/1HuWLNhYB-IOflkUaE5d84KNCFW-QXl2ATyTQV5lwu8U/edit?usp=sharing)
- **Corresponding authors:**
  - Dr. Steven J. Bethard (bethard@arizona.edu)
  - Dr. Tracy E. Crane (tecrane@med.miami.edu)
- **Social Media**
  - [Twitter #cranelab](https://twitter.com/search?q=%23cranelab&src=typed_query)
  - [@sylvestercancer](https://twitter.com/SylvesterCancer)
  - [@DrTracyECrane](https://twitter.com/DrTracyECrane)

### Cite as

Sarah Freylersythe, Rebecca Sharp, John Culnan, Damian Yukio Romero Diaz, Yiyun Zhao, G. Hagan Franks, Remo Nitschke, Steven J. Bethard, and Tracy E. Crane. 2022. Lessons Learned from a Secondary Analysis Using Natural Language Processing and Machine Learning from a Lifestyle Intervention: SBM Conference Handout. Retrieved from https://github.com/clulab/SBM_2022_LIvES

*Note: This citation is in [ACM format](https://www.acm.org/publications/authors/reference-formatting). For different formatting options, please use the "`Cite this repository`" button on the right menu of this repository, along with a BibTeX converter such as this one: [Online Bibtex Converter](https://asouqi.github.io/bibtex-converter/).*

## Conference Handout

### Background

- We faced ***challenges related to data re-usability*** while working on a secondary analysis of the Lifestyle Intervention for oVarian cancer Enhanced Survival (***LIvES***), GOG 0225.

- The LIvES Study tested whether a behavioral lifestyle intervention of increased physical activity and a healthy diet would increase progression-free ovarian cancer survival compared to an attention control [1].

- Our goal during the secondary analysis was to automate fidelity scoring and prediction of lifestyle behavioral outcomes through natural language processing (NLP) and machine learning (ML).

- In this presentation, we describe the issues we faced and the lessons we learned. ***We believe our experience will interest anyone planning to work on health interventions in our age of machine learning and artificial intelligence.***

### Data

- The original data was collected during the LIvES study, a behavioral lifestyle intervention that used trained health coaches and Motivational Interviewing (MI), a directive, patient-centered counseling approach to increase progression-free ovarian cancer survival.

#### Planned study data (LIvES original data)

- Demographics, anthropometrics, and actigraphy collected at the start of the study
- Additional anthropometric and actigraphy data collected at 6, 12, and 24-month marks
- Recorded telephone coaching sessions (approximately 24,500) in English and Spanish from 1205 women participating in the study were used for analysis. None were transcribed or diarized (data derivatives)
- 323 of the recorded coaching sessions were scored for adherence to MI techniques and study fidelity but not stored in a machine-friendly format

#### Additional data needed for secondary NLP/ML analysis

- Coaching sessions needed to be re-scored for adherence to MI techniques and study fidelity
- Data derivatives needed to be created (recording transcriptions and diarizations)
- Data links between recordings, fidelity data, and study outcomes were missing

#### Massive untapped study data

- Computer-mediated coach/participant interactions such as emails and SMSs
- Participant food and activity journals not stored in a machine-friendly format
- Coaching call notes not stored in a machine-friendly format
- Probably more


![Iceberg figure](https://github.com/clulab/SBM_2022_LIvES/blob/main/visuals/iceberg_figure.png)

### Challenges

Numerous costly measures were taken to re-use our data:

| Challenge     | Workaround     | Cost     | Recommendation  |
| :-----------: | :------------: | :------: | :-------------: |
| Lack of data and file centralization E.g., (1) Audio files and fidelity scores were not linked to study outcomes (2) Using Drupal instead of a dedicated database | (1) Manual linking using inconsistent, secondary identifiers (2) Post-hoc creation of a database system with many gaps | 3 Specialists with HIPAA training performing manual work for approximately 240 hrs. 606 of 1,870 links between data were unrecoverable | Use unique identifiers and a database to centralize all data and files, not only the ones relevant to your current study |
| Lack of planning for data derivatives. E.g., (1) Using non-machine-friendly data annotation methods (2) Missed opportunities to collect audio diarizations from original study (3) Missed opportunities to use personnel expertise for usable data | Training personnel to re-do what experts had already done (MITI scores and fidelity scores), plus assigning new personnel to do tasks that original personnel were already doing but not recording | Approximately 170 hrs. of manual work, including training of new personnel and data re-annotation | Plan for machine-friendly data structure and format. Co-collect data and data derivatives: if the study personnel are generating data derivates, find ways to collect them. If possible, use the expertise of the study personnel to generate additional data that might be helpful for future research.|
| Incomplete socio-cultural background data. E.g., No language, cultural or socio-cultural background information collected in the LIvES demographics | Use proxies (e.g., language preference) whenever possible. Proxies are seldom free of confounding factors, so data must be carefully interpreted | Missed opportunities for analysis. E.g., Missing acculturation information for Latina participants does not allow for between-group comparisons, and we needed to use language preference (Spanish vs. English) as proxies [2] | Collect culturally relevant data in all studies. If possible, survey the population or estimate its characteristics using census data before any intervention takes place. |
| No de-identification of HIPAA data. E.g., Personally identifiable information was still present in the audio files from the LIvES study | (1) Setting up a HIPAA-compliant HPC cloud system (2) Work with smaller, compressed ML models, which sacrifice accuracy (3) Manual de-identification was needed in certain cases | Analysis turnaround was delayed because of the need to secure HIPAA-compliant high-performance computers | Create data de-identification protocols for all data types. |
| Consenting only participants. E.g., Coaches' consent was not obtained in the original LIvES study  | Re-consent coaches | 40 hrs. of work and in some cases we could not get in touch with some of the coaches which means the data was lost | Consent all the people involved, not only participants. |

### Discussion

- The LIvES study data was not prepared for NLP/ML analyses
  - The data infrastructure for the original LIvES study, due to its long-running nature, evolved in ways that lost data continuity
  - The data alignment process would have been simplified by establishing a single identifier to link calls, outcomes, and MITI scores and maintaining that identifier over the course of the project
  - Evaluating the quality of automated transcription systems is difficult and could have been streamlined by manually transcribing a small number of study calls to be used for evaluation
  - Data de-identification would have simplified NLP/ML analyses. Because current Transformer-based models for NLP "can be too large and computationally intensive to run on standard deployments" [3], non-de-identified data needs to run on HIPAA compliant high-performance computers, which are more difficult to set up, especially within an academic institution.
  - Training a machine learning model to assess interviewer turns could have been simplified by establishing a protocol for coding MITI scoring using an annotation tool, resulting in turn-level annotations alongside the holistic scoring typical of MITI

- Numerous steps were necessary to prepare the natural language processing and machine learning analyses
  - Data were aligned manually through a combination of participant phone numbers, coach names and participant names, entry dates, and recording dates
  - Transcription was performed both manually and then automatically with wav2vec [4]
  - The reliability of the automatic transcription was poor, so we developed a process to improve its accuracy using speaker turn detection, which required manual annotation
  - An annotation interface was developed using Label Studio for speaker turn identification and content coding
  - Coding guidelines were developed for Motivational Interviewing Treatment Integrity (MITI) 3.0 and protocol fidelity
  - Due to lack of data de-identification, we had to perform ML/NLP analyses using researchers' personal computers with limited, non-state of the art compressed ML models
  - We set up a HIPAA-compliant infrastructure for data annotation and to improve ML analyses
  - We developed a data management plan to help us avoid previous mistakes [5]. The data management plan is [publically available](https://dmptool.org/plans/74502/export.pdf?export[question_headings]=true) for other researchers to consult

- Actionable data management foresight
  - Beyond being a requirement, traditional data management plans are extremely helpful in data governance and for making data re-usable
  - Comprehensive data re-usability is critical for machine learning and artificial intelligence analysis and development
  - Traditional data management for health interventions must be taken one step further to plan for interfacing with current and future technologies even if these would not be used in the current study
  - Biomedical datasets are not well-documented and not easily incorporated into popular machine learning frameworks [6]. Although [ongoing efforts](https://github.com/bigscience-workshop/biomedical) are trying to change this, we suggest that all health interventions apply the FAIR principles of Findability, Accessibility, Interoperability, and Reusability to help accelerate this process [7]

### Conclusion

- Actionable data management foresight can help extract value from non-traditional sources of data from behavioral health interventions
- To take advantage of machine learning, natural language processing and artificial intelligence, behavioral interventions should engage the support of a data scientist in the study design planning stage and throughout data collection.

### Acknowledgment of financial support

This work was supported by the following grants:

- [LIvES Study (GOG 0225) NCT00719303](https://clinicaltrials.gov/ct2/show/NCT00719303)
- BMISR UACC P30 CA023074
- NLP/ML NIH/NCI 1R21CA256680-01 (MPI: Tracy E. Crane/Steven J. Bethard)

### References

[1]Cynthia A. Thomson, Tracy E. Crane, Austin Miller, David O. Garcia, Karen Basen-Engquist, and David S. Alberts. 2016. A randomized trial of diet and physical activity in women treated for stage II–IV ovarian cancer: Rationale and design of the Lifestyle Intervention for Ovarian Cancer Enhanced Survival (LIVES): An NRG Oncology/Gynecologic Oncology Group (GOG-225) Study. Contemporary Clinical Trials 49, (July 2016), 181–189. DOI:https://doi.org/10.1016/j.cct.2016.07.005

[2]Irlena Alejandra Penaloza. 2020. Responsiveness to Motivational Interviewing Among Latina Ovarian Cancer Survivors Participating in a Large, Well Powered RCT: A Mixed Methods Analysis. phdthesis. University of Arizona, Tucson, Arizona. Retrieved from http://hdl.handle.net/10150/642195

[3]Eldar Kurtic, Daniel Campos, Tuan Nguyen, Elias Frantar, Mark Kurtz, Benjamin Fineran, Michael Goin, and Dan Alistarh. 2022. The Optimal BERT Surgeon: Scalable and Accurate Second-Order Pruning for Large Language Models. arXiv:2203.07259 [cs] (March 2022). Retrieved April 5, 2022 from http://arxiv.org/abs/2203.07259

[4]Steffen Schneider, Alexei Baevski, Ronan Collobert, and Michael Auli. 2019. wav2vec: Unsupervised Pre-training for Speech Recognition. CoRR abs/1904.05862, (2019). Retrieved from http://arxiv.org/abs/1904.05862

[5]Damian Yukio Romero Diaz. 2022. Using natural language processing to determine predictors of healthy diet and physical activity behavior change in ovarian cancer survivors. (2022). DOI:https://doi.org/10.48321/D1BK5T

[6]BigScience Workshop. BigScience Biomedical (BIGBIO) NLP Hackathon. Retrieved April 5, 2022 from https://hfbigbio.github.io/

[7]Mark D. Wilkinson, Michel Dumontier, IJsbrand Jan Aalbersberg, Gabrielle Appleton, Myles Axton, Arie Baak, Niklas Blomberg, Jan-Willem Boiten, Luiz Bonino da Silva Santos, Philip E. Bourne, Jildau Bouwman, Anthony J. Brookes, Tim Clark, Mercè Crosas, Ingrid Dillo, Olivier Dumon, Scott Edmunds, Chris T. Evelo, Richard Finkers, Alejandra Gonzalez-Beltran, Alasdair J.G. Gray, Paul Groth, Carole Goble, Jeffrey S. Grethe, Jaap Heringa, Peter A.C ’t Hoen, Rob Hooft, Tobias Kuhn, Ruben Kok, Joost Kok, Scott J. Lusher, Maryann E. Martone, Albert Mons, Abel L. Packer, Bengt Persson, Philippe Rocca-Serra, Marco Roos, Rene van Schaik, Susanna-Assunta Sansone, Erik Schultes, Thierry Sengstag, Ted Slater, George Strawn, Morris A. Swertz, Mark Thompson, Johan van der Lei, Erik van Mulligen, Jan Velterop, Andra Waagmeester, Peter Wittenburg, Katherine Wolstencroft, Jun Zhao, and Barend Mons. 2016. The FAIR Guiding Principles for scientific data management and stewardship. Scientific Data 3, (March 2016). DOI:https://doi.org/10.1038/sdata.2016.18

## License

The content of this repository is distributed freely under a Creative Commons 4.0 International license (CC by 4.0). You are free to share and adapt as long as you use the work correctly, provide a link to the license, and indicate if changes were made. The full license can be found at [https://creativecommons.org/licenses/by/4.0/legalcode](https://creativecommons.org/licenses/by/4.0/legalcode).

![CC by 4.0 logo](https://i.creativecommons.org/l/by/4.0/88x31.png)
