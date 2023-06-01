# opensw23-ten
Text-To-Speech project
## Team Introduction
  김영준 : 201911162 리더  
  박상준 : 201911173 코더  
  신민석 : 202011316 github expert  
  김수형 : 202211276 발표자  
## Topic Introduction
### References
## Topic Introduction
https://github.com/fatchord/WaveRNN

저희가 선택한 오픈소스는 TTS입니다.

TTS(Text to Speech)는 '음성합성'으로 일정한 음성 단위로 분할한 후 입력받은 텍스트를 따라 필요한 음성단위들을 이어 붙여 말소리를 인위적으로 만들어 내는 기술입니다. 
python quick_start.py -u --input_text "샘플 텍스트" 커맨드를 사용해 사용자가 입력한 샘플 텍스트를 음성으로 바꿔줍니다.
자신만의 모델을 트레이닝 시킬 수 있습니다.

샘플데이터를 사용한 Result는 아래와 같습니다.
## Results
https://opensw23-ten.github.io/sample/
## Analysis/Visualization

## Installation
Python >= 3.6
Pytorch 1(1.0.0) with CUDA
pip를 이용하여 나머지를 설치 합니다 :
  pip install -r requirements.txt

## Use
# Quick Start
빠르게 간단한 결과를 얻고 싶으면 quik_start를 이용합니다:
  python quick_start.py -u --input_text "샘플데이터"
# Trainin own Models
1 - Tacotron을 트레이닝시킵니다:
  python train_tacotron.py

2 - 트레이닝이 끝나거나 언제든지 끝낼 수 있습니다(이렇게 하면 훈련이 완료되지 않은 경우에도 택트론이 GTA 데이터 세트를 강제로 생성합니다.):
  python train_tacotron.py --force_gta

3 - WaveRNN을 트레이닝시킵니다:
  python train_wavernn.py --gta

참고: TTS에 관심이 없다면 --gta 없이 train_wavernn.py만 실행해도 됩니다.

4 - 두 모델을 모두 사용하여 문장 생성하기
기본 문장 생성:
  python gen_tacotron.py wavernn
사용자 지정 문장 생성:
  python gen_tacotron.py --input_text "넣고싶은 input text" wavernn

(언제든지 해당 스크립트에서 --help를 사용하여 사용 가능한 옵션을 확인할 수 있습니다.)


## Presentation
