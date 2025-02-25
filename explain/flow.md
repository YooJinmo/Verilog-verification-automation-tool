# 🚀 Verilog Simulation & Verification Process

## 📌 개요
이 문서는 **Verilog 파일 생성부터 검증 및 결과 비교까지의 전체 프로세스**를 설명합니다. 
해당 과정은 자동화되어 있으며, GitHub Actions 또는 로컬 환경에서 실행 가능합니다.

## 🔄 실행 단계

### 1️⃣ **Verilog 파일 생성**
- **(1) Generate `adder.v`**
- **(2) `generate_vfile.py` 실행** → `adder_n.v` 생성
- **(3) `generate_tb.py` 실행** → `adder_tb.v` 생성

### 2️⃣ **입력 데이터 생성 (`input.txt`)**
- **(1) `generate_input.py` 실행**
- **(2) `edge_case.py` 실행** (테스트 케이스 확장)
- **(3) `input.txt` 생성** (테스트 데이터 포함)

### 3️⃣ **Verilog 시뮬레이션 실행**
- **(1) `adder_n.v` 실행**
- **(2) `adder_tb.v` 실행**
- **(3) `verilog_output.txt` 생성** (Verilog 시뮬레이션 결과 저장)

### 4️⃣ **Python Adder 실행**
- **(1) `run_python_adder.py` 실행**
- **(2) `python_output.txt` 생성** (Python으로 Full Adder 실행 결과 저장)

### 5️⃣ **결과 비교 및 CSV 저장**
- **(1) `compare_files.py` 실행** (Verilog vs Python 결과 비교)
- **(2) `txt_to_csv.py` 실행** (비교 결과를 CSV 형식으로 변환)
- **(3) `comparison_output.csv` 저장**

### 6️⃣ **성공률 계산**
- **(1) `success_per.py` 실행** (비교 결과를 분석하여 성공률 계산)
- **(2) `success_per.txt` 생성** (성공률 결과 저장)
