# iipl_nlp_toy

9, 10 - Goal : Submission

## Issue : Kernels-only competition

지금까지 해왔던 submission.csv 파일을 제출해서 평가하는 방식이 아닌 Kaggle Kernels 상에서 평가를 받는 방식

(Data Download Issue 라고 생각)

만든 파일을 github 에 업로드 후 Kaggle 에서 URL upload 를 통한 Notebook Load

Kaggle Kernel 상에서 데이터 경로가 상대적으로 다음과 같음 

> '../input/quora-insincere-questions-classification/train.csv'

output file 은 별다른 경로 지정안해줘도 제대로 생성

* Kaggle Kernels GPU Quota 40hours *

## Issue : conda env kernel 

콘다 가상환경 사용 후 남아있는 kernel 정보가 Kaggle 세션에서 새로 갱신되지 않고 유지되어 Save 진행시 NoSuchKernel error 를 리턴한다.

결과 로그상으로 남아있어서 세션은 다 돌았는데, output file 이 없어서 제출을 못함 

처음에 사용했던 콘다 가상환경을 기본 Python3 로 변경 후 저장하면 kernel 정보가 Python 으로 변하기 때문에 커널 정보가 바뀐 소스를 사용하면 됨

