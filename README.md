# ai_detection_keystroke_logs
Plagiarism Detection Using Keystroke Logs 

This repository contains data from

Crossley, S. A., Tian, Y., Holmes, L., Morris, W., & Choi, J. S. (2024). [Plagiarism Detection Using Keystroke Logs.](https://educationaldatamining.org/edm2024/proceedings/2024.EDM-short-papers.47/2024.EDM-short-papers.47.pdf) Proceedings of the 17th International Conference on Educational Data Mining (EDM). Atlanta, GA.

There are two files

ai_detection_essays_scores_sim_anon_github.csv

This contains the essays, the human scores, and the similarity scores between the original essays and their transcriptions.

ai_detect_keystroke_logging_data_anon_github.csv

This contains all the keystroke logging metrics.

Information about the data collection methods is below

**METHOD**
	
We collected essays and keystroke logs from crowd-sourced workers in two different time periods. Initially, we collected authentic essays from 4,992 participants. From these authentic essays, we selected 500 essays that were highly scored. We then had crowd-sourced workers transcribe these essays while also collecting their keystroke logs.

**2.1	Authentic Data Collection**

*2.1.1	Participants*

Participants were hired from Amazon Mechanical Turk (MTurk), an online crowdsourcing platform that enables large-scale participant recruitment in a time-efficient manner. Data was collected prior to November, 2022, when ChatGPT was released. Participants were selected based on the following criteria: 1) be at least 18 years old; 2) be currently living in the United States; 3) have completed at least 50 MTurk tasks with an overall approval rate of at least 98% by requesters on the platform. 

*2.1.2	Procedure*

Participants hired from MTurk were invited to log onto a web-site built specially for this study. The website housed a demo-graphic survey, a series of typing tests, an argumentative writ-ing task, and a vocabulary knowledge test. Participants were required to use only computers with a keyboard to participate in the study. Their keystroke activities during the typing tests and the argumentative writing task were recorded using a built-in keystroke logging program that captured every keystroke and mouse operation entered by the participants with its timestamp and cursor position information. Participants' role in the study lasted 40-50 minutes. Their participation was compensated by a $0.25 reward and a $11.75 bonus upon completing all the tasks following the instructions.

*2.1.3	Argumentative Writing*

In the argumentative writing task, participants were asked to write an argumentative essay within 30 minutes in response to a writing prompt adapted from a retired Scholastic Assessment Test (SAT) taken by high school students attempting to enter post-secondary institutions in the United States. To control for potential prompt effects, four SAT-based writing prompts were used, and each participant was randomly assigned one prompt. Prior to the writing task, participants were given in-structions about how to write an argumentative essay and sug-gested that participants should write an essay of at least 200 words in 3 paragraphs and that they should not use any online or offline reference materials.

*2.1.4	Apparatus*

To collect participants' keystroke information during the typ-ing tests and the argumentative writing task, a keystroke log-ging program was written in JavaScript and was embedded in the script of the website built for this study. The program un-obtrusively recorded every keystroke operation and mouse activity along with relevant timing and cursor position infor-mation when participants completed typing tasks and wrote their essays. It also simultaneously identified operation types (e.g., input, delete, paste, replace) and reported text changes in the writing process. Table 1 provides an example output of keystroke logging information reported by the program. Event ID indexes the keyboard and mouse operations in chronologi-cal order. Down Time denotes the time (in milliseconds) when a key or the mouse was pressed while Up Time indicates the release time of the event. Action Time represents the duration of the operation (i.e., Up Time - Down Time). Position registers cursor position information to help keep track of the location of the leading edge. Pause Time demonstrates the time inter-vals between consecutive events (i.e., IKIs). Word Count dis-plays the accumulated numbers of words typed in. Additional-ly, Text Change shows the exact changes made to the current text while Activity indicates the nature of the changes (e.g., Input, Remove/Cut). 
Unlike keystroke logging software widely used in writing research (e.g., ScriptLog, Inputlog), this web-based program can be easily deployed in any browser-based writing environment and thus avoids inconveniences associated with installing or updating any software beyond a standard web browser. It is also highly scalable and well-suited for online keystroke in-formation collection using crowdsourcing. In terms of privacy concerns, the logging capacity of this program is confined to the input fields on the webpages for the typing tests and the argumentative writing task, and hence does not track any other information as participants operate on their computers throughout the experiment.

*2.1.5	Essay Collection and Scoring*

We collected 4,992 acceptable essays from the crowd-sourced workers. To ensure the essays were of high quality and, thus, similar to essays that would be produced by generative AI, the essays were scored by trained raters for overall writing quality using a holistic, six-point grading scale commonly used in assessing essays written for college admission in the United States (i.e., the SAT scoring rubric). The SAT rubric evaluates writing quality on multiple dimensions, including test-takers’ development of a point of view on the issue, evidence of criti-cal thinking, use of appropriate examples, accurate and adapt use of language, the variety of sentence structures, errors in grammar and mechanics as well as text organization and coher-ence. Essays were randomly assigned among six raters and each essay was scored by two raters. The raters were graduate students majoring either in English or applied linguistics. All of them had at least two years of experience teaching English composition at the university level. All raters went through at least three rounds of training sessions before they scored the essays independently. The training started off with a briefing about the essay collection methods and the holistic rubric, followed by a discussion of potential biases in essay scoring. For each session, raters were asked to score a batch of essays on their own before they met to discuss the differences in their scores. A total of 60 practice essays were used for training purposes. These practice essays were on the same topics but were sampled from a different dataset. The raters exited the training sessions and started independently scoring the essays only after a satisfying agreement had been reached for the prac-tice essays with a Cohen's Kappa of at least .600 [7]. After scoring the entire data, the Cohen's Kappa = 0.759, p < .001, suggesting substantial overall agreement between the raters. If score differences between two raters were two points or great-er, the raters adjudicated the scores through discussion. If agreement was not reached, the score was not changed. Average scores between the raters for the adjudicated holistic scores were calculated for each essay.

We selected 500 essays from the larger corpus of 4,992 essays that were of higher quality and thus would better reflect essays produced by generative AI. All essays were scored by at least one rater as 4 (indicating an above average essay). Overall, the essays reported scores of M = 3.94, SD = .40. The essays were written on four prompts that we generally distributed equally. The mean length of the essays was 364.852 (SD = 112.309). On average, the essay contained 4.44 paragraphs (SD = 1.471).

**2.2	Transcribed Data Collection**

*2.2.1	Participants*

Participants were hired from Amazon Mechanical Turk (MTurk). Participants were required to meet three threshold qualifications: 1) be at least 18 years old; 2) be currently liv-ing in the United States; 3) have an overall approval rate of at least 95% by requesters on the platform.

*2.2.2	Procedure*

Participants hired from MTurk were invited to log onto a web-site built specially for this study. The website housed a demo-graphic survey and a transcribing task. Participants were re-quired to use desktop computers with a keyboard to partici-pate in the study. Their keystroke activities during the typing tests and the argumentative writing task were recorded using the same built-in keystroke logging program as in the argumen-tative essay collection. 
For the transcribing task, participants were randomly assigned an essay from the 500 higher quality essays. The assigned es-say was presented on the transcribing task page in tandem with a transcribing area. Prior to transcribing, participants were in-structed to transcribe the authentic text verbatim following a set of rules. These rules included 1) avoiding the use of any intelligent grammar and spell checkers and 2) refraining from irrelevant activities during transcription. Figure 1 below shows the transcription screen presented to the participants.

We conducted checks to ensure the accuracy of the data. First, we examined the keystroke data and removed flawed logs (e.g., logs with record of copying and pasting the original essay or Irrelevant activities during transcribing). Second, we calculat-ed the string similarity between the transcribed essay and the authentic essay using the levenshteinSim function (a similari-ty function derived using the Levenshtein distance) from the RecordLinkage R package [19]. In order for the transcription to be accepted, a string similarity threshold of .95 and .90 were set. All essays scoring above the .95 threshold were accepted without further inspection. Essays that scored above the .90 threshold but below .95 were inspected manually for missing sentences. If multiple sentences were found to be missing, the data was rejected. These thresholds ensured that the tran-scribed essay accurately reflected the original. Out of the 63 transcribed essays within this threshold range, five essays were missing more than three sentences from the original essay and were not accepted into the final batch. These essays were collected from different Mechanical Turk workers so that we had transcribed data for all 500 essays.

*2.3	Keystroke Logging Measures*

The keystroke logging files were transformed into IDFX files that could be read and analyzed via Inputlog 7.0 [24]. A set of keystroke indices with reference to the participants' produc-tion fluency, bursts, pausing behaviors, revision activities, and process variances were generated from the keystroke logs collected from the authentic writers and the transcribed writ-ers. In total, 155 keystroke logging measures were developed.

*2.3.1	Production Fluency*

We analyzed participants’ production fluency during writing or transcribing using Inputlog’s summary analysis. The report-ed measures included means, medians, and standard deviations for the number of different linguistic units (i.e., characters, words, sentences, paragraphs) produced per minute in text production. Note that these measures were calculated based on the writing/transcribing process rather than the final product and thus included any deleted text.

*2.3.2	Bursts*

Measures of P-bursts (bursts that ended with a pause longer than two or more seconds) were obtained by drawing on the summary analysis provided by Inputlog. In this study, P-bursts were operationalized as continuous text production episodes terminated at pauses of 2 or more seconds, following the rationale that pauses exceeding 2 seconds generally corre-sponding to higher-level thinking processes such as activities related to planning, and thus eliminating the interruptions caused by transcription-related activities or inefficiencies in motor execution [28]. To obtain measures of R-bursts (bursts that ended with grammatical discontinuities such as revi-sions), revision analysis was performed to calculate the num-bers and lengths of bursts delimited by revision activities.

*2.3.3	Pauses*

We generated two sets of pause measures using Inputlog's pause analysis based on two different thresholds: 200 milli-seconds and 2 seconds. We adopted these two thresholds be-cause the former has the strength of capturing the bulk of lan-guage- and planning-related differences in pausing and filtering most inter-key intervals that result solely from the motor con-straint of typing [16], while the latter generally reflects higher order cognitive processes, such as planning for new ideas or revising [14]. We also analyzed pauses at different locations (e.g., within words, between words, between sentences) be-cause they are associated with various patterns of pausing behaviors and might provide insights into different underlying cognitive processes in writing [5].

*2.3.4	Revisions*

Revisions were analyzed by drawing on the revision matrix reported by Inputlog. The revision matrix provides a detailed list of revision events in sequential order. Inputlog distin-guishes between two types of revision events: 1) deletions, i.e., characters deleted in the text produced so far, and 2) inser-tions, which represents the characters inserted into the earlier text. In this study, we calculated the total numbers of dele-tions and insertions and also developed a set of measures re-garding the length of deletions and insertions in characters and words.

*2.3.5	Process Variances*

To take into account the variability of each participant's entire writing process, variances in process fluency were investigated using Inputlog's fluency analysis which reports production rates (characters produced per minute) at different stages in the writing process. In this study, we analyzed process variances with the number of intervals set at 5 or 10 respectively (i.e., the entire writing time for each essay was divided evenly into 5 or 10 segments). We adopted the standard deviation values reported by Inputlog as a measure of process variance to de-scribe how dispersed the production rate for each interval in relation to the mean value.

This data is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).
