<div align="center">

# 김도근 · Kim Do-guen

**On-Device AI Semiconductor & Embedded Systems Engineer**

MCU 펌웨어부터 FPGA RTL, Edge AI 추론 최적화까지<br>
연산이 일어나는 가장 아래 계층을 설계하고 검증합니다.

<a href="mailto:kimdk1005@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
<a href="tel:010-3905-3964"><img src="https://img.shields.io/badge/010--3905--3964-2E7D32?style=flat-square" alt="Phone"></a>
<a href="https://www.youtube.com/@Xenonex11038"><img src="https://img.shields.io/badge/시연영상-FF0000?style=flat-square&logo=youtube&logoColor=white" alt="YouTube"></a>

</div>

---

### 🛠 Tech Stack

| | |
|---|---|
| **Language · Tools** | <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/Verilog-1A73E8?style=flat-square"> <img src="https://img.shields.io/badge/SystemVerilog-174EA6?style=flat-square"> <img src="https://img.shields.io/badge/Tcl-9C6B30?style=flat-square"> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"> |
| **FPGA · SoC** | <img src="https://img.shields.io/badge/Vivado%20%2F%20Vitis-E48400?style=flat-square&logo=xilinx&logoColor=white"> <img src="https://img.shields.io/badge/MicroBlaze%20V-C8102E?style=flat-square&logo=amd&logoColor=white"> <img src="https://img.shields.io/badge/AXI4--Lite-6A1B9A?style=flat-square"> <img src="https://img.shields.io/badge/Basys3%20(Artix--7)-0071C5?style=flat-square&logo=xilinx&logoColor=white"> |
| **Embedded** | <img src="https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white"> <img src="https://img.shields.io/badge/ATmega128A-EF7C00?style=flat-square"> <img src="https://img.shields.io/badge/FreeRTOS-3C9C35?style=flat-square&logo=freertos&logoColor=white"> <img src="https://img.shields.io/badge/STM32CubeIDE-00A9E0?style=flat-square"> |
| **Edge AI · Vision** | <img src="https://img.shields.io/badge/YOLOv11-111F68?style=flat-square"> <img src="https://img.shields.io/badge/NCNN-FF6F00?style=flat-square"> <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"> <img src="https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white"> |
| **Interface** | `AXI4-Lite` `UART` `CAN(MCP2515)` `I2C` `SPI` `BLE` `PWM` `ADC+DMA` `GPIO/EXTI` |
| **Method** | `RTL 설계·Testbench 검증` `Timing Closure` `IP Packaging·Block Design` `FreeRTOS Task/Mutex/Queue` `Non-blocking FSM` |

---

### 🚀 Projects

| 프로젝트 | 기술 | 핵심 구현 |
|---|---|---|
| **[EdgeScope-Lite SoC](https://github.com/kimdk1005-collab/EdgeScope-Lite-SoC)**<br><sub>2026.08 · 3인팀</sub> | SystemVerilog · Vivado/Vitis<br>MicroBlaze V · Basys3 (Artix-7) | CPU 폴링 1.67 MS/s를 **하드웨어 100 MS/s 등간격 캡처**로 전환 — Probe Sampler IP 설계·SoC 통합 담당 |
| **[MimicArm](https://github.com/kimdk1005-collab/MimicArm-FPGA-Project)**<br><sub>2026.06 · 3인팀</sub> | Verilog · Vivado<br>Basys3 (Artix-7) | BRAM IP·나눗셈 없이 **D-FF 레지스터 뱅크**로 Teach & Playback 로봇팔 구현 |
| **[Object-Detecting Autonomous Taxi](https://github.com/kimdk1005-collab/Object-Detecting-Autonomous-Taxi)**<br><sub>2026.07 · 3인팀</sub> | YOLO11n · NCNN<br>Raspberry Pi · STM32F446 · CAN | 학습 해상도 640→320 재조정으로 **탐지 지연 2초 해소** |
| **[Beyond Control (3-Way RC Car)](https://github.com/kimdk1005-collab/3-Way-RC-Car)**<br><sub>2026.06 · 개인</sub> | STM32F411 · FreeRTOS<br>BLE · ADC+DMA | 스마트폰·자율주행·전용 컨트롤러를 **3-Way 제어로 통합** |
| **[Touch-free Elevator](https://github.com/kimdk1005-collab/Touch-Free-Elevator)**<br><sub>2026.05 · 3인팀</sub> | STM32F411RE<br>Non-Blocking FSM | 비접촉 IR 호출 + **방향성 SCAN 배차 알고리즘** 구현 |
| **[Smart Fish Tank](https://github.com/kimdk1005-collab/Smart-Fish-Tank)**<br><sub>2026.05 · 4인팀</sub> | ATmega128A<br>Dual-MCU | 조도센서 **차분(DIFF) 방식 탁도 측정**으로 저가 센서 정확도 보완 |

> 📺 전체 시연 영상 → **[YouTube](https://www.youtube.com/@Xenonex11038)** ｜ 각 저장소에 설계 의도와 트러블슈팅을 문서화해 두었습니다.

---

### 🎓 Education

- **대한상공회의소 경기인력개발원** — 온디바이스 AI 반도체설계 3기 · 2026.02 ~ 2026.09 (940h)
- **울산대학교** 공과대학 첨단소재공학부 재료공학 전공 · 2020.03 ~ 2026.08 (졸업예정)

### 📜 Certifications & Awards

`ADsP` `컴퓨터활용능력 2급` `TOEIC Speaking IH(140)` `1종 보통 운전면허`

🏆 캡스톤디자인 『남김없이 깨끗한 화장품 용기』 — **대상**(첨단소재공학부장상) · **우수상**(울산대학교 총장상), 2022.12

---

<div align="center">

> 재료공학 기반의 소재 이해와 임베디드·반도체 설계 역량을 결합해,<br>
> **온디바이스 AI 시대의 하드웨어를 직접 설계하고 검증하는 엔지니어**로 성장하겠습니다.

</div>
