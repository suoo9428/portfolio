# Portfolio

## About Me
- **Name**: [김수민]
- **Field**: 데이터과학 / 데이터분석
- **Skills**: Python, R, SQLite, Tableau, Machine Learning, WEKA, VADER


## Project
### 프로젝트 개요
본 연구는 남극 및 북극 연구소에 있는 연구자들의 감정 표현을 분석하기 위해 Mastodon 소셜 미디어 게시글의 감정 분석을 수행했습니다.

### 연구 요약
본 연구는 극한 환경에서의 감정 표현에 영향을 미치는 성별 차이와 플랫폼 특성을 조사하며, 심리적 회복력을 높이기 위한 성별 맞춤형 지원 시스템의 필요성을 강조합니다. VADER 감정 분석을 통해 남성과 여성의 감정 표현 방식이 어떻게 다른지 파악합니다.

### 데이터 수집
- **플랫폼**: Mastodon, Twitter
- **샘플 수**: 남극 및 북극 연구소 관계자의 게시물 1,545개, NASA 우주비행사 Twitter 게시물 1,545개(random sampling).
- **사용 도구**: Python, VADER 감정 분석

### 분석 방법
- VADER를 사용하여 각 게시물의 긍정, 중립, 부정, 종합감정을 점수화했습니다.
- VADER 종합점수(compound score)는 다음과 같은 기준으로 해석됩니다:
  - +0.05 이상: 긍정적인 감정
  - -0.05 이하: 부정적인 감정
  - -0.05 에서 +0.05 사이: 중립적인 감정
- 성별에 따른 감정 차이를 T-test로 분석
- 플랫폼에 따른 감정 표현 차이를 T-test로 분석

### 주요 결과
[성별에 따른 감정표현 차이]

![T_test_results_gender](https://github.com/user-attachments/assets/e90e7258-e6dc-45c7-ac39-3aa866a60a92)
- compound score(종합점수) : 여성의 compound score 평균이 0.2037, 남성의 compound score 평균이 0.2406로, 전체적인 감정 강도 차이가 통계적으로 유의미 하지 않음(p > 0.05).
- positive score(긍정점수) : 여성의 긍정 점수 평균(0.1952)이 남성(0.1323)보다 높으며(p < 0.05), 여성은 더 긍정적인 표현을 많이 사용함.
- neutral score(중립점수) : 남성의 중립 점수 평균(0.8298)이 여성(0.7376)보다 유의미하게 높아(p < 0.05), 남성이 여성보다 중립적 감정을 더 자주 표현하는 경향 나타냄.
- negative score(부정점수) : 여성의 부정 점수 평균(0.0672)이 남성(0.0379)보다 높으며(p < 0.05), 여성은 부정적 감정을 더 많이 표현하는 경향이 있음.

[플랫폼에 따른 감정표현 차이]

![t_test_results_platform](https://github.com/user-attachments/assets/557e574e-213d-440e-a20e-68cb9e0a1b6a)
- positive score(긍정점수)  : Twitter의 긍정 점수 평균(0.1818)이 Mastodon(0.1594)보다 유의미하게 높음(p = 0.0015). 이는 Twitter에서 긍정적 감정 표현이 더 많이 나타나는 경향을 시사함.
- neutral score(중립점수) : 중립 감정 점수의 평균에는 유의미한 차이가 없으며(p = 0.7955), Twitter와 Mastodon 모두 중립적 감정이 비슷한 빈도로 나타남.
- negative score(부정점수) : Mastodon의 부정 점수 평균(0.0505)이 Twitter(0.0228)보다 유의미하게 높음(p < 0.05). 이는 Mastodon에서 부정적 감정이 더 자주 표현되는 경향이 있음.
- compound score(종합점수) : Twitter의 compound 점수 평균(0.3470)이 Mastodon(0.2251)보다 유의미하게 높음(p < 0.05). 이는 Twitter에서 전반적으로 더 긍정적인 감정 표현이 많다는 것을 의미함.
* Twitter: 0.3470 > +0.05 (긍정적 감정)
* Mastodon: 0.2251 > +0.05 (긍정적 감정)


[중립적 감정의 우세]

![Distribution of compound sentiment scores](https://github.com/user-attachments/assets/4e6a3bbf-25c5-4eca-807e-9f52dddf4943)
- 중립 감정의 우세: 그래프에서 compound score가 0 근처에 빈도가 높게 집중되어 있음. 이는 대체로 중립적인 감정 표현이 많이 나타남.
- 긍정으로 약간 치우친 분포: 평균(mean)과 중앙값(median)이 약 0.23으로, 약간 긍정적인 방향으로 치우쳐 있음. 이는 전체적으로 중립에 가깝지만 다소 긍정적인 감정 표현이 더 많다는 의미로 해석됨.

![Distribution of Postiie, neutral, and negative sentiment scores](https://github.com/user-attachments/assets/0e20fc87-23a6-476e-93de-c14eecc6eab3)
- 중립 감정의 우세 : 중립 감정 점수(회색)가 가장 높은 빈도로 나타나며 특히 1.0에 해당하는 높은 빈도가 눈에 띔. 이는 중립적인 감정 표현이 매우 많이 사용되었음을 시사함.
- 부정 감정의 초기 빈도 높음 : 부정 감정 점수(빨간색)가 0 근처에서 상대적으로 높은 빈도로 나타남. 이는 부정적인 감정 표현이 많지만, 그 강도가 낮다는 것을 의미함.
- 긍정 감정의 낮은 빈도 : 긍정 감정 점수(초록색)는 부정 및 중립 감정에 비해 전반적으로 빈도가 낮음. 이는 긍정적인 감정 표현이 상대적으로 덜 사용되었음을 의미함.


### 결론
본 연구는 극한 환경에서의 감정 표현에 있어 성별에 따른 지원 시스템을 구축하고, 감정표현에 있어 유연한 미디어 플랫폼을 만드는 것을 장려합니다.
