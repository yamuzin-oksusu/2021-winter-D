# 2021-winter-D 
[2021년 동계 컨퍼런스] 키워드 기반 금융 정보 요약 서비스 구현 

금융 소비자 권익 제고를 위한 AI Solution을 제안합니다. (NLP)

약관의 키워드를 추출하기 전에, 형태소 분석기를 통해 명사만 추출한 문서를 만들어주었습니다. (KoNLPy의 오픈 소스 한국어 형태소 분석기 Okt 이용)

위와 같은 방법으로 전처리를 끝낸 문서를 가지고, KeyBERT의 extract_keywords() 모듈을 이용해 키워드를 추출했습니다. keyphrase_ngram_range 인자를 조정해 한 단어부터 세 단어까지의 키워드를 추출했습니다. stop_words 인자를 통해 불용어를 설정해줄 수 있는데, 은행명과 같이 자주 등장하여 모델이 중요하다고 판단할 확률이 높지만 사실상 별 의미가 없는 단어들을 불용어로 설정해주었습니다.

## 팀원 소개

김민주 (경영학, 4)
Minjoo Kim (Business Administration, Senior)

김민지 (응용통계학, 4)

이건이 (응용통계학, 3)
