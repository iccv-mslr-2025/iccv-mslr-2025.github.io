---
layout: default
class: page-challenge
---

# 🏆 Challenge Tracks

## 🌊 Track 1: Continuous Sign Language Recognition

We will use the Isharah dataset to organize this competition.  
The dataset consists of 30,000 video clips representing 2,000 unique sign language sentences performed by 18 signers. Two sub-tasks will be used in this challenge: signer-independent and unseen sentences. In addition, two modalities will be provided for researchers: video and pose information. The dataset paper will be available on arXiv in June 2025.

## 🌊 Track 2: Isolated Sign Language Recognition

The competition will utilize our proprietary dataset.  
The dataset consists of 100 signs and 26 letters covering both medical and general-purpose vocabulary. Each sign is recorded 205 times, with synchronized data from RGB video, radar sensors, facial keypoints, and skeletal tracking. The subset track will provide only 20 repetitions per sign to facilitate few-shot learning research. Participants can compete emphasizing different aspects of multimodal fusion:  
- **Radar + Face Data**: Techniques that combine RGB data and radar information to capture subtle non-manual cues.

---

# Challenge Rules

## Registration

Teams who want to join the challenge can register by sending an email to raffaele.mineo[at]unict.it and hluqman[at]kfupm.edu.sa indicating the team name and for each participant:
- Name
- Surname
- Affiliation
- Email

## Evaluation Criteria and Methodology

The performance of the submitted models will be evaluated using the following criteria:
- **Track 1 (Continuous Sign Challenge)**: Balanced accuracy score on the held-out-trials test set.
- **Track 2 (Isolated Sign Language)**: Balanced accuracy score on the held-out-trials test set.

In the event of a tie, the originality of the approach will be used as an additional criterion, with the organizers taking responsibility for the final decision.

Participants are allowed to submit results for one or both tasks. We will select the top-5 performing teams, based on the distribution of participants among the tasks.

## Guidelines for Participants

- Participants can submit their predictions up to five times. Only the last one is considered.
- Participants can submit to either one track or both.
- All submissions should be accompanied by a brief (1-page) description of the employed method.
- The top 5 ranked teams per track will be invited to submit a paper, to be presented at ICCV 2025, which should be submitted before the Challenges Submission deadline.
- Participants will be ranked according to the best performance for every single task. If two teams get the same score, the ranking will be determined by the innovation of the employed methods.
- Each participant can only be included in one participating team.
- Participants can use the full training set to train the models for both tasks.
- Test data cannot be used during training. The test sets can be used only to provide output predictions. All parameters should be tuned on the training set. Participants can derive validation sets from the training set.
- We encourage all teams to publicly share their code at the end of the contest.

### Use of External Data

The use of external data (both training data and/or pretrained models) is allowed, if all conditions are met:
- The datasets, or pretrained models, are publicly and freely available.
- Datasets/pretrained models must be available before the start of this challenge.
- Datasets/model weights used to generate predictions must be cited in the final description and in the final paper.
- Public pretrained models, trained on private data, can be used only after the approval of the organizers.

## Submission Guidelines

Each team should submit their predictions by e-mailing raffaele.mineo[at]unict.it and hluqman[at]kfupm.edu.sa.

### Submission Email Structure

Each submission email MUST include the following:
- The challenge track and team name in both the subject line and body of the email.
- At least one attached `.csv` file containing predictions. File naming conventions and instructions can be found below in the Submission File Structure section.
- An attached one-page `.pdf` file briefly explaining the methodology used. This document is free-form and will not be published. Only challenge winners will be required to submit a paper.

Each participating team is permitted up to five submissions per task and may choose to submit for one or both tasks. Any team member can submit the final results on behalf of the team. Each email containing result files will count as a single submission.

### Submission File Structure

We expect a single `.csv` file named `teamName_trackNumber_test.csv` for the held-out-trial test set.

Each `.csv` file should contain only two columns:
- `id`: the sample ID
- `prediction`: the predicted class

Here is an example of the structure:
```
id,prediction
0,12
1,19
2,8
```

Ensure all files adhere to this format to meet the submission requirements.
