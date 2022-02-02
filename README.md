# ShowmetheMusic

보아즈 Adv proejct 쇼미더뮤직팀 '텍스트 감정추출을 통한 노래 추천 시스템' 프로젝트 깃허브입니다.

## 주제소개

## 선정배경

## 모델링 아키텍처

## NLP 모델링

## 추천시스템 모델링


### - 1차 추천

![추천1](https://user-images.githubusercontent.com/76245088/152142565-b8ea8bae-3624-40f1-81d8-743d7b3345dd.jpg)

- 사용자에게 감정과 가사의 중요도를 INPUT으로 받아 감정과 가사에 가중치를 반영하여 글과 유사한 노래순으로 나열
- 사용자에게 감정과 유사한, 감정과 반대되는 노래를 제공
- 사용자의 선택에 따라 데이터셋 고정 

### - 2차 추천

![추천2](https://user-images.githubusercontent.com/76245088/152143461-6ff44945-f263-48fc-a0d8-0c41073d799f.jpg)

- 1차 추천에서 사용자가 선택한 데이터셋에서 감정과 가사의 중요도를 반영하여 텍스트와 가장 유사한 노래 5곡을 추천
- 사용자에게 5곡에 대한 5점 척도의 점수를 받음 
- 사용자가 가장 높은 점수를 준 노래의 8가지 감정값을 GET
- 해당 감정값과 노래 데이터 사이의 유사도를 계산
- 계산된 유사도를 기반으로 노래 데이터셋을 재정렬하고 유사도를 기반으로 재추천

### - 노래 추천 프로세스 

![추천3](https://user-images.githubusercontent.com/76245088/152144213-b6b02bae-53d2-4744-b2d9-6dceb0575bbb.jpg)

- NLP모델을 활용해 기쁨, 분노, 슬픔의 세가지 감정 중 사용자의 텍스트가 어디에 해당하는지 분류
- 사용자에게 노래를 추천받을 때, 감정과 가사 중 어떤것을 더 중요시 여기는지 5점척도로 입력을 받음
- 사용자가 입력한 중요도를 함께 고려하여 텍스트와 유사도를 기반으로 정렬함
- 텍스트의 감정과 유사한 감정을 가지는 노래, 반대되는 감정을 가지는 노래를 추천하여 사용자의 선택에 따라 데이터 고정
- 유사도 top 5인 노래를 재추천하고, 사용자에게 추천에 대한 평가를 5점 척도로 받아 가장 높은 점수의 노래를 기반으로 다른 노래와의 유사도를 계산하여 5곡씩 반복하여 추천

## 결론 및 제언
