<div align="center">

# 김도근 · Kim Do-geun

### On-Device AI Semiconductor & Embedded Systems Engineer

<p>
  <img src="https://img.shields.io/badge/MCU-STM32%20%7C%20AVR-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white" alt="MCU">
  <img src="https://img.shields.io/badge/FPGA-Verilog%20RTL-0071C5?style=flat-square" alt="FPGA">
  <img src="https://img.shields.io/badge/RTOS-FreeRTOS-3C9C35?style=flat-square&logo=freertos&logoColor=white" alt="FreeRTOS">
  <img src="https://img.shields.io/badge/Edge%20AI-YOLO%20%7C%20NCNN-FF6F00?style=flat-square" alt="Edge AI">
</p>

**소재를 이해하는 재료공학 기반 위에 임베디드·반도체 설계 역량을 쌓아,<br>온디바이스 AI 시대의 하드웨어를 직접 설계하고 검증하는 엔지니어를 지향합니다.**

</div>

---

## About Me

울산대학교 첨단소재공학부에서 **재료공학**을 전공하고, 대한상공회의소 경기인력개발원 **온디바이스 AI 반도체설계 3기** 과정을 통해 임베디드 시스템과 RTL 설계를 다루고 있습니다.

MCU 펌웨어부터 FPGA RTL, Edge AI 추론 최적화까지 **"연산이 일어나는 가장 아래 계층"** 에 관심이 있습니다. 프로젝트를 진행할 때는 동작하는 코드를 만드는 것에서 멈추지 않고, **왜 이 구조를 선택했는지**를 설명할 수 있는 설계를 목표로 합니다.

- 이론적인 계산값과 실제 하드웨어의 차이를 **실측으로 보정**하는 과정을 중요하게 생각합니다.
- Blocking 코드를 **인터럽트·상태 머신 기반의 Non-Blocking 구조**로 바꾸는 설계를 즐깁니다.
- 정상 동작뿐 아니라 **비정상 종료 경로(Fail-Safe)** 까지 설계 범위로 봅니다.

---

## Tech Stack

| 분류 | 기술 |
|---|---|
| **MCU / Firmware** | STM32F4 시리즈 (STM32CubeIDE · CubeMX · HAL), ATmega128A (AVR-GCC) |
| **FPGA / RTL** | Verilog RTL, Xilinx Vivado, Basys3 (Artix-7) |
| **RTOS** | FreeRTOS — Task 분리, Mutex, Message Queue, 우선순위 설계 |
| **통신 프로토콜** | UART / USART, CAN (MCP2515), I2C, SPI, BLE |
| **Edge AI** | YOLOv11, ONNX, NCNN, OpenCV |
| **Language** | C, Python, Verilog |
| **Tools** | Git / GitHub, VSCode, STM32CubeIDE, Vivado |

<p>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black" alt="C">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Verilog-1A73E8?style=flat-square" alt="Verilog">
  <img src="https://img.shields.io/badge/STM32CubeIDE-00A9E0?style=flat-square" alt="STM32CubeIDE">
  <img src="https://img.shields.io/badge/Vivado-E48400?style=flat-square&logo=xilinx&logoColor=white" alt="Vivado">
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white" alt="Raspberry Pi">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git">
</p>

---

## Projects

정밀 제어 · 자율주행 · 임베디드 IoT 순으로 정리했습니다. 각 저장소에 설계 의도와 트러블슈팅 과정을 문서화해 두었습니다.

> 📺 전체 프로젝트 시연 영상은 **[YouTube 채널](https://www.youtube.com/@Xenonex11038)** 에서 보실 수 있습니다.

### 🦾 [MimicArm — FPGA Teach & Playback 로봇팔](https://github.com/kimdk1005-collab/MimicArm-FPGA-Project)

`Verilog RTL` `Vivado` `Basys3 (Artix-7)` · 2026.06 · 3인팀

작업자가 조작한 자세를 저장한 뒤 부드럽게 재생하는 로봇팔을 **순차회로만으로** 구현했습니다.

- **XADC · BRAM IP · 나눗셈 연산자를 모두 배제**하고 D-FF 기반 레지스터 뱅크로 자원(LUT) 최적화
- PWM 듀티 계산을 상수화하여 나눗셈을 곱셈으로 대체, 증분 보간으로 속도를 틱 주기로 정의
- 3관절이 모두 목표에 도달했을 때만 진행하는 **이벤트 정렬 Dwell** 구조 설계
- 담당: 하드웨어 설계, PWM 제어 및 증분보간 로직

### 🚕 [Object-Detecting Autonomous Taxi](https://github.com/kimdk1005-collab/Object-Detecting-Autonomous-Taxi)

`YOLO11n` `NCNN` `Raspberry Pi 4B` `STM32F446RE` `FreeRTOS` `CAN` · 2026.07 · 3인팀

비전 인식과 실시간 제어를 **CAN 버스로 연결한 이기종 시스템**입니다.

- 학습 해상도 최적화(640 → 320)로 약 2초의 탐지 지연을 실주행 가능 수준으로 개선
- 스쿨존 맥락 기억 · 횡단보도 쿨다운 · 신호등 우선순위를 갖춘 **주행 판단 FSM** 설계
- 브릿지 비정상 종료 시 **STOP 명령 3회 강제 송신**하는 Fail-Safe 로직
- 담당: YOLO11n 모델 학습, ONNX 변환 파이프라인 구축, NCNN Edge 추론 최적화

### 🚗 [Beyond Control — 3-Way RC Car](https://github.com/kimdk1005-collab/3-Way-RC-Car)

`STM32F411` `FreeRTOS` `BLE` `ADC + DMA` · 2026.06 · 개인 프로젝트

스마트폰 · 자율주행 · 전용 컨트롤러의 **세 가지 주행 모드를 하나의 플랫폼에 통합**했습니다.

- `MotorTask` / `SensorTask` / `CommTask` 분리 및 Queue · Mutex 기반 동기화
- 좌우 초음파 거리 오차 기반 **P 제어**로 복도 중앙 유지, Deadband·Clamp로 조향 안정화
- 조이스틱 4채널을 ADC Scan + Circular DMA로 연속 취득하는 전용 컨트롤러 제작

### 🛗 [Touch-free Elevator](https://github.com/kimdk1005-collab/Touch-Free-Elevator)

`STM32F411RE` `Non-Blocking FSM` `IR Sensor` · 2026.05 · 3인팀

적외선 비접촉 호출과 **방향성 SCAN 배차 알고리즘**을 적용한 4층 엘리베이터입니다.

- 상승·하강·내부 호출을 3개 큐로 분리하여 실제 엘리베이터의 배차 동작 재현
- TIM 인터럽트에서 Half-step을 1스텝씩 출력해 **이동 중에도 입력·표시가 멈추지 않는 구조**
- 담당: 스텝모터 층 이동 제어, FND 층 표시, 하드웨어 제작, 발표

### 🐠 [Smart Aquarium Automation System](https://github.com/kimdk1005-collab/Smart-Fish-Tank)

`ATmega128A` `AVR-GCC` `Dual-MCU` · 2026.05 · 4인팀

전용 센서 없이 **조도센서와 LED의 차분(DIFF) 측정**으로 탁도를 정량화했습니다.

- 주변광 기준값과 투과광 측정값의 차이를 사용해 조명 환경 변화의 영향을 상쇄
- 블로킹 서보 구동을 **별도 MCU로 분리**하고 2선 GPIO 핸드셰이크로 연동
- 담당: 자동 먹이 배급 모듈 구현, 하드웨어 제작

---

## Education

| 기간 | 내용 |
|---|---|
| 2026.02 ~ 2026.09 | 대한상공회의소 경기인력개발원 **온디바이스 AI 반도체설계 3기** (940시간) |
| 2020.03 ~ 2026.08 | **울산대학교** 공과대학 첨단소재공학부 재료공학 전공 (2026년 8월 졸업예정) |

---

## Certifications & Awards

### Certifications

| 자격 | 취득 |
|---|---|
| ADsP (데이터분석 준전문가) | 2026.03 |
| 컴퓨터활용능력 2급 | 2024.07 |
| TOEIC Speaking IH (140) | 2025.11 |
| 1종 보통 운전면허 | 2020.01 |

### Awards

**캡스톤디자인 『남김없이 깨끗한 화장품 용기』** — PLA 기반 분리형·리필형 화장품 용기 설계 (3D프린팅 · FDM 공정)

- 🥇 **대상** — 첨단소재공학부장상 (첨단소재공학부 캡스톤디자인 경진대회, 2022.12)
- 🥈 **우수상** — 울산대학교 총장상 (울산대학교 캡스톤디자인 경진대회, 2022.12)

---

## Career Vision

> 재료공학 기반의 소재 이해와 임베디드·반도체 설계 역량을 결합해,
> **온디바이스 AI 시대의 하드웨어를 직접 설계하고 검증하는 엔지니어**로 성장하겠습니다.

소자와 회로, 펌웨어와 알고리즘을 각각 따로 보는 것이 아니라, 하나의 시스템으로 연결해 이해하는 엔지니어가 되는 것이 목표입니다.

---

<div align="center">

### Contact

<a href="mailto:kimdk1005@gmail.com">
  <img src="https://img.shields.io/badge/kimdk1005@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email">
</a>
<a href="tel:01039053964">
  <img src="https://img.shields.io/badge/010--3905--3964-2E7D32?style=flat-square" alt="Phone">
</a>
<a href="https://www.youtube.com/@Xenonex11038">
  <img src="https://img.shields.io/badge/시연%20영상-FF0000?style=flat-square&logo=youtube&logoColor=white" alt="YouTube">
</a>
<a href="https://github.com/kimdk1005-collab">
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub">
</a>

**Embedded Firmware · FPGA RTL · Edge AI · Real-Time Control**

</div>
