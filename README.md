# 2022 OUTTA AI Bootcamp final project
![AI coaching for facial expression](./AIcoaching.PNG)

이 프로젝트는 2022 제 1회 OUTTA AI 부트캠프의 최종 팀 프로젝트를 위한 스켈레톤 코드입니다.<br>
<br>
이 프로젝트는 자신이 연기하고 싶은 일상생활 속의 한 마디나 영화 대사 등을 입력하고, 웹캠을 바라보며 표정 연기를 하면 표정 연기의 점수를 화면에 출력하는 프로젝트입니다.<br>
<br>
이번 프로젝트에서는 Pytorch와 OpenCV를 사용하여 간단한 인공지능 프로그램을 구현해보는 것을 목표로 합니다.<br>
<br>
이번 프로젝트를 위해서는 업로드 되어있는 9개의 ipynb 파일 중에서 main_stream_final.ipynb 파일을 제외한 모든 파일을 수정하셔야 합니다.<br>
<br>
이 프로젝트에 대한 자세한 가이드라인 및 평가 기준은 '참고pdf 폴더 안에' 업로드되어 있는 3개의 pdf 파일들을 참고하시길 바랍니다.<br>
- 최종미션 안내 (08.13.).pdf<br>
- Guideline.pdf <br>
- Part 5 최종미션 채점기준.pdf <br>
<br>
이 프로젝트는 Google Colab 환경과 Anaconda 환경에서 시행되는 것을 기본으로 하여 제작되었습니다.<br>
<br>

# Dataset
데이터셋은 다음의 [링크](https://drive.google.com/drive/folders/1_QSPldD9hAnZNykS36_AXYRsFE19A8cY?usp=sharing)에서 다운로드 받을 수 있습니다.<br>
<br>
이 프로젝트는 2개의 데이터셋을 사용하였습니다.
## 1. FER2013
FER2013 데이터셋은 Facial Emotion Recognition을 위해 제안된 데이터셋입니다.<br>
<br>
이 데이터셋이 처음 소개된 논문은 Ian J. Goodfellow 등이 작성한 Challenges in Representation Learning: A report on three machine learning contests 입니다. [논문: Challenges in Representation Learning: A report on three machine learning contests](https://paperswithcode.com/paper/challenges-in-representation-learning-a)<br>

### 1-1. 폴 에크만의 보편 감정 6가지
<br>
심리학자인 폴 에크만은 문화나 학습에 따라 달라지지 않는 보편적인 감정과 그에 대응되는 표정이 있다는 연구 결과를 제시했고, 인류의 보편적인 감정을 6가지(공포, 기쁨, 놀람, 분노, 슬픔, 혐오)로 분류하였습니다.<br>
<br>
대부분의 감정 관련 AI 연구는 폴 에크만의 연구에 기반하여 수집된 데이터셋을 사용합니다. 물론 사람의 감정을 6가지로만 분류하는 관점에 대해 비판적인 시각도 있으며, 표정과 감정의 상관관계에 대해서도 불확실한 부분들이 있습니다.<br>
<br>
그럼에도, 이 팀 프로젝트에서는 기존의 감정 관련 AI 연구의 관행에 따라 폴 에크만의 감정 분류 체계를 따르는 AI를 개발해보았습니다.<br>

### 1-2. FER2013 데이터셋 구성
<br>
FER 2013은 폴 에크만의 보편 감정 6가지에 중립(neutral)을 더한 7가지 라벨로 구성되어 있습니다.<br>
<br>
모든 이미지는 48x48 pixel 사이즈의 흑백 이미지이며, 데이터셋에서 각 감정에 대응되는 인덱스는 영어 알파벳 순으로 (0,분노) (1,혐오) (2,공포) (3,기쁨) (4,중립) (5,슬픔) (6,놀람) 입니다.<br>
<br>
이 데이터셋은 무료 오픈 데이터셋으로, Kaggle 회원가입 후 무료로 다운받아 이용할 수 있습니다. 데이터셋이 업로드되어 있는 링크로는 다음 두가지를 찾아볼 수 있고, 이 팀 프로젝트에서는 csv 형식의 파일을 사용하였습니다.<br>
- [낱장의 이미지 파일들](https://www.kaggle.com/datasets/msambare/fer2013)
- [csv 파일](https://www.kaggle.com/datasets/deadskull7/fer2013)

## 2. 한국어 감정 정보 대화 데이터셋


