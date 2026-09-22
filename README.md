<div align="center">

# 김도근 · Kim Do-guen

**On-Device AI Semiconductor & Embedded Systems Engineer**

MCU 펌웨어부터 FPGA RTL, Edge AI 추론 최적화까지<br>
연산이 일어나는 가장 아래 계층을 설계하고 검증합니다.

<a href="mailto:kimdk1005@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://www.youtube.com/@Xenonex11038"><img src="https://img.shields.io/badge/시연영상-FF0000?style=flat-square&logo=youtube&logoColor=white" alt="YouTube"></a>

</div>

---

### 🛠 Tech Stack

<table>
<tr>
<td><b>Language&nbsp;·&nbsp;Tools</b></td>
<td>
<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black">
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Verilog-1A73E8?style=flat-square">
<img src="https://img.shields.io/badge/SystemVerilog-174EA6?style=flat-square">
<img src="https://img.shields.io/badge/Tcl-9C6B30?style=flat-square">
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
</td>
</tr>
<tr>
<td><b>FPGA&nbsp;·&nbsp;SoC</b></td>
<td>
<img src="https://img.shields.io/badge/Vivado%20%2F%20Vitis-E48400?style=flat-square&logo=xilinx&logoColor=white">
<img src="https://img.shields.io/badge/Zynq--7000%20(Zybo%20Z7--20)-0071C5?style=flat-square&logo=xilinx&logoColor=white">
<img src="https://img.shields.io/badge/MicroBlaze%20V-C8102E?style=flat-square&logo=amd&logoColor=white">
<img src="https://img.shields.io/badge/AXI4--Lite-6A1B9A?style=flat-square">
<img src="https://img.shields.io/badge/Basys3%20(Artix--7)-0071C5?style=flat-square&logo=xilinx&logoColor=white">
</td>
</tr>
<tr>
<td><b>Embedded</b></td>
<td>
<img src="https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white">
<img src="https://img.shields.io/badge/ATmega128A-EF7C00?style=flat-square">
<img src="https://img.shields.io/badge/FreeRTOS-3C9C35?style=flat-square&logo=freertos&logoColor=white">
<img src="https://img.shields.io/badge/ARM%20Cortex--A9-0091BD?style=flat-square&logo=arm&logoColor=white">
<img src="https://img.shields.io/badge/STM32CubeIDE-00A9E0?style=flat-square">
</td>
</tr>
<tr>
<td><b>Edge&nbsp;AI&nbsp;·&nbsp;Vision</b></td>
<td>
<img src="https://img.shields.io/badge/TensorFlow%20%2F%20Keras-FF6F00?style=flat-square&logo=tensorflow&logoColor=white">
<img src="https://img.shields.io/badge/YOLOv11-111F68?style=flat-square">
<img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white">
<img src="https://img.shields.io/badge/NCNN-FF6F00?style=flat-square">
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white">
<img src="https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white">
</td>
</tr>
<tr>
<td><b>Interface</b></td>
<td>
<code>AXI4-Lite</code> <code>UART</code> <code>CAN(MCP2515)</code> <code>I2C</code> <code>SPI</code> <code>BLE</code> <code>PWM</code> <code>ADC+DMA</code> <code>GPIO/EXTI</code>
</td>
</tr>
<tr>
<td><b>Method</b></td>
<td>
<code>RTL 설계·Testbench 검증</code> <code>Timing Closure</code> <code>IP Packaging·Block Design</code> <code>INT8 양자화</code> <code>FreeRTOS Task/Mutex/Queue</code> <code>Non-blocking FSM</code>
</td>
</tr>
</table>

---

### 🚀 Projects

| 프로젝트 | 기술 | 핵심 구현 |
|---|---|---|
| **이벤트 카메라 기반 실시간 객체 추적**<br><sub>2026.09 · 3인팀</sub> | Verilog · Vivado/Vitis<br>Zybo Z7-20 (Zynq-7000)<br>ARM Cortex-A9 · AXI4-Lite | 프레임 차분 **이벤트 텐서 전처리**와 히트맵 좌표 기반 **Dead Zone + P 제어**로 4축 Pan/Tilt 추적 구현<br><sub>담당 — 이벤트 입력·전처리, 추적 제어 및 서보/레이저 구동, 안전 인터록(각도 제한·E-stop·REARM), 하드웨어 제작·최종 시연 / Tiny CNN 학습·INT8 양자화·Python↔RTL 비교 검증 공동 참여</sub><br><sub>시스템 성과 — PL NPU 추론 1.258 ms (ARM 대비 약 7.8배), INT8 정확도 92.02%</sub><br>🏆 **대상** — 대한상공회의소 경기인력개발원장상 |
| **[Object-Detecting Autonomous Taxi](https://github.com/kimdk1005-collab/Object-Detecting-Autonomous-Taxi)**<br><sub>2026.07 · 3인팀</sub> | YOLO11n · NCNN<br>Raspberry Pi · STM32F446 · CAN | 학습 해상도 640→320 재조정으로 **탐지 지연 2초 해소**<br><sub>담당 — YOLO11n 학습 · NCNN Edge 추론 최적화, 차량 전장 설계·제작 총괄</sub> |
| **[MimicArm](https://github.com/kimdk1005-collab/MimicArm-FPGA-Project)**<br><sub>2026.06 · 3인팀</sub> | Verilog · Vivado<br>Basys3 (Artix-7) | 비교기·카운터 증분 보간으로 **나눗셈기 제거**, LUT 사용량 최적화<br><sub>담당 — PWM 서보 제어, 증분 보간 로직, 하드웨어 설계·전원 배선</sub> |
| **[Beyond Control (3-Way RC Car)](https://github.com/kimdk1005-collab/3-Way-RC-Car)**<br><sub>2026.06 · 개인</sub> | STM32F411 · FreeRTOS<br>BLE · ADC+DMA | 스마트폰·자율주행·전용 컨트롤러를 **3-Way 제어로 통합**<br><sub>담당 — 기획·회로 구성·펌웨어·제어 알고리즘 전 범위 단독 구현</sub> |
| **[Touch-free Elevator](https://github.com/kimdk1005-collab/Touch-Free-Elevator)**<br><sub>2026.05 · 3인팀</sub> | STM32F411RE<br>Non-Blocking FSM | 비접촉 IR 호출 + **방향성 SCAN 배차 알고리즘** 구현<br><sub>담당 — 스텝모터 층간 이동 제어, FND 층 표시, 하드웨어 제작</sub> |
| **[Smart Fish Tank](https://github.com/kimdk1005-collab/Smart-Fish-Tank)**<br><sub>2026.05 · 4인팀</sub> | ATmega128A<br>Dual-MCU | 조도센서 **차분(DIFF) 방식 탁도 측정**으로 저가 센서 정확도 보완<br><sub>담당 — 자동 먹이 배급 모듈 구현, 하드웨어 제작</sub> |

> 📺 전체 시연 영상 → **[YouTube](https://www.youtube.com/@Xenonex11038)** ｜ 각 저장소에 설계 의도와 트러블슈팅을 문서화해 두었습니다.

---

### 🎓 Education

- **대한상공회의소 경기인력개발원** — 온디바이스 AI 반도체설계 3기 · 2026.02 ~ 2026.09 (940h, 수료)
- **울산대학교** 공과대학 첨단소재공학부 재료공학 전공 · 2020.03 ~ 2027.02 (졸업예정)

### 📜 Certifications & Awards

`ADsP` `컴퓨터활용능력 2급` `한국사능력검정시험 2급` `TOEIC Speaking IH(140)` `1종 보통 운전면허`

🏆 온디바이스 AI 반도체설계 과정 프로젝트 발표회 — **대상**(대한상공회의소 경기인력개발원장상), 2026.09<br>
🏆 캡스톤디자인 『남김없이 깨끗한 친환경 화장품 용기』 — **대상**(첨단소재공학부장상) · **우수상**(울산대학교 총장상), 2022.12

---

<div align="center">

> 재료공학 기반의 소재 이해와 임베디드·반도체 설계 역량을 결합해,<br>
> **온디바이스 AI 시대의 하드웨어를 직접 설계하고 검증하는 엔지니어**로 성장하겠습니다.

</div>
