# portfolio

## About Me
- **Name**: [김수민]
- **Field**: Data Science(데이터과학) / 분석
- **Skills**: Python, R, SQLite, Tableau, Machine Learning, WEKA


## Project
### 프로젝트 개요
본 연구는 남극 및 북극 연구소에 있는 연구자들의 감정 표현을 분석하기 위해 Mastodon 소셜 미디어 게시글의 감정 분석을 수행했습니다.

### 연구 요약
본 연구는 극한 환경에서의 감정 표현에 영향을 미치는 성별 차이와 플랫폼 특성을 조사하며, 심리적 회복력을 높이기 위한 성별 맞춤형 지원 시스템의 필요성을 강조합니다. VADER 감정 분석을 통해 남성과 여성의 감정 표현 방식이 어떻게 다른지 파악합니다.

### 데이터 수집
- **플랫폼**: Mastodon, Twitter
- **샘플 수**: 남극 및 북극 연구소 관계자의 게시물 1,545개, NASA 우주비행사 Twitter 게시물 1,545개(random sampling)
- **사용 도구**: Python, VADER 감정 분석

### 분석 방법
- VADER를 사용하여 각 게시물의 긍정, 중립, 부정 감정을 점수화했습니다.
- 성별에 따른 감정 차이를 T-test로 분석
- 플랫폼에 따른 감정 표현 차이를 T-test로 분석
- 

### 주요 결과
- 성별에 따른 감정표현 차이
![T_test_results_gender](https://github.com/user-attachments/assets/e90e7258-e6dc-45c7-ac39-3aa866a60a92)

- 플랫폼에 따른 감정표현 차이
![t_test_results_platform](https://github.com/user-attachments/assets/557e574e-213d-440e-a20e-68cb9e0a1b6a)



- 극한 환경에서의 감정표현은 중립 감정이 주를 이루었고, 남성은 여성보다 더 중립적인 감정을 표현하는 경향이 있었습니다.
![Distribution of Postiie, neutral, and negative sentiment scores](https://github.com/user-attachments/assets/0e20fc87-23a6-476e-93de-c14eecc6eab3)
![Distribution of compound sentiment scores](https://github.com/user-attachments/assets/4e6a3bbf-25c5-4eca-807e-9f52dddf4943)


### 결론
본 연구는 극한 환경에서의 감정 표현에 있어 성별에 따른 지원 시스템을 구축하고, 감정표현에 있어 유연한 미디어 플랫폼을 만드는 것을 장려합니다.
