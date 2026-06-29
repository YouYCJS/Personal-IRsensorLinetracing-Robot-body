# Personal-IRsensorLinetracing-Robot-body
# Autonomous Line-Tracing Robot Mainboard
**RP2040 기반 IR 라인트레이싱 로봇 메인보드**

> Raspberry Pi Pico(RP2040)와 TB6612 모터 드라이버로 4채널 IR 센서를 읽어
> 자율주행하는 라인트레이싱 로봇 메인보드. 섀시 일체형 커스텀 PCB로 설계했습니다.
> 
<img src="https://github.com/user-attachments/assets/ff5d3243-92b3-4d79-9757-4b218302e6c9" alt="완성 보드 3D 앞면" width="55%">

## 개요
4개의 IR 센서로 바닥 라인을 읽고, TB6612 드라이버로 두 모터를 제어해
자율주행하는 로봇의 메인 제어 보드입니다. 보드 외형을 로봇 섀시 형태로 설계해
별도 프레임 없이 센서·구동부·전원을 한 보드에 통합했습니다.

## 구성
- **메인 컨트롤러**: Raspberry Pi Pico (RP2040)
- **모터 드라이버**: DFRobot TB6612
- **센서**: IR 센서 ×4 (IR_1 ~ IR_4, AN/DI 출력)
- **전원**: XT30 입력 + 토글 스위치 + 레귤레이터(com-18357, 3.3V)
- **구동부**: DC 모터 ×2 (JL / JR 커넥터)
- **설계 툴**: Altium Designer

## 이전 버전 대비 개선점
- **MCU**: Arduino → Raspberry Pi Pico (RP2040), 처리 성능·PWM 채널 확보
- **모터 드라이버**: L293D → TB6612, 효율·발열 개선
- **센서**: 단일 IR → 4채널 IR, 정밀 라인 추종
- **구조**: 범용 사각 보드 → 섀시 일체형 외형 설계

## 완성된 보드

| 앞면 (3D) | 뒷면 (3D) |
|:---:|:---:|
| <img src="https://github.com/user-attachments/assets/ff5d3243-92b3-4d79-9757-4b218302e6c9" alt="3D 앞면" width="100%"> | <img src="https://github.com/user-attachments/assets/01fc82f3-749a-4db9-be57-7e52be9e60e4" alt="3D 뒷면" width="100%"> |

## 설계 과정

1. 회로 설계 (스키매틱) — Pico, TB6612, 4채널 IR, 전원부
2. PCB 레이아웃 — 섀시 일체형 외형, 양면 라우팅
3. 3D 뷰로 부품 배치·풋프린트 검증
4. 제조 발주

| 회로 설계 (Schematic) | PCB 레이아웃 |
|:---:|:---:|
| <img src="https://github.com/user-attachments/assets/af9c5777-b89e-4c67-8d9b-ac229106d193" alt="스키매틱" width="100%"> | <img src="https://github.com/user-attachments/assets/64875ac5-c9c8-4a21-96db-528a086906b7" alt="PCB 레이아웃" width="100%"> |

## 회고
- L293D 기반 입문작 대비 MCU·드라이버·센서·구조 전반을 고도화
- 보드 외형을 로봇 섀시로 설계해 기구·전자 통합 경험
