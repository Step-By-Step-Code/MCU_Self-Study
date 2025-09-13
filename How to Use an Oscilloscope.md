# Oscilloscope

## Oscilloscope 구조
### Probe → Attenuator
- 프로브에서 신호가 처음 도착
- 전압이 크면 내부 회로가 망가질 수 있어 감쇠함

### Amplifier 증폭
- 감쇠된 신호나 작은 신호를 증폭
- Volts/div[수직]를 조절할 수 있음

### Trigger
- 신호가 계속 움직이면 분석이 힘듬
- 기준점을 줘서 파형이 화면에 고정되도록 함

### AD Converter
- 증폭된 아날로그 신호를 디지털 값으로 변환

### Memory
- 변환된 디지털 데이터는 메모리에 저장
- 메모리 깊이가 깊을수록 더 긴 시간동안의 파형을 저장/분석 가능

### Timebase System
- 파형이 얼마나 빨리/느리게 표시될지 결정
- Time/div[수평]
- 샘플 데이터를 시간축에 맞춰 배열해주는 역할

### Display DSP
- 메모리에 저장된 데이터를 DSP로 처리하고 화면에 파형을 그림

-------------------------------
## How to use a Oscilloscope
### 채널 별 설정 요소

#### Open CH
- 채널을 켜거나 끄는 기능
#### Open FFT
- 주파수 영역 분선 [ 스펙트럼 분석 ] 볼 수 있음
#### Coupling
- DC coupling : 직류와 교류 성분 모두 같이 보여줌
- AC coupling : 직류 성분을 차단하고 교류 성분만 보여줌
 
#### Probe Mode
- 오실로스코프 프로브 감쇠 설정
- 1X 신호를 그대로 읽음 [ 대역폭 낮음, 고주파 신호 왜곡 가능 ]
- 10X 신호를 1/10로 줄여서 입력 [고주파 신호 정확히 측정 가능, 노이즈 줄어듦]
- 100X 매우 높은 전압 측정 시 사용

### Trigger
- Trigger Mode
    - **Auto**
        - Trigger 조건에 만족되면 파형을 표시
        - 일정시간마다 화면을 갱신해 파형이 흘러가는 것처럼 보여줌
    - **Normal**
        - 트리거 조건이 만족될 때만 화면을 갱신, 조건이 맞지 않으면 화면 멈춤
        - 조건에 맞는 파형만 볼 수 있음
    - **Single**
        - 트리거 조건이 한 번 만족되면 한 번 캡처하고 화면을 멈춤
        - 순간적인 신호 잡을 때만 사용
        - 다시 캡쳐하려면 RUN/STOP 눌러야함
- Trigger Edge [Rising / Falling]
- Trigger CH : Trigger 할 채널 선택