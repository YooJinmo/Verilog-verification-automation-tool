### Verilog-verification-automation-tooㅣ
---
1. 전체 구조 (파일 간 관계)
- - generate_input.py	: 랜덤 8비트 입력값(A, B) 생성 및 저장 (input.txt)
  - run_verilog.py : Verilog 시뮬레이터 실행 자동화 (iverilog & vvp)
  - testbench.v : Verilog 테스트벤치 (Python에서 제공한 입력값을 읽고 결과 출력)
  - dut.v : 실제 Verilog 설계 파일 (Design Under Test, DUT)
---
2. Python으로 입력 데이터 생성(generate_input.py)
---
3. Verilog 테스트벤치 작성 (testbench.v)
---
4. Verilog 설계 파일 (dut.v)
---
5. Python에서 Verilog 실행 (run_verilog.py)
