# 📅 IOS Scheduler App

iOS 앱 프로젝트: 사용자로부터 날짜 및 시간을 입력받고, 선택한 시간에 대한 확인 및 메모를 남길 수 있는 간단한 스케줄 관리 앱입니다.

---


## 📌 프로젝트 개요

- **프로젝트명**: Scheduler
- **개발환경**: Xcode, Swift, UIKit
- **주요 기능**:
  - 사용자가 UIDatePicker로 날짜 및 시간 선택
  - 선택한 날짜를 Alert 창으로 확인
  - 선택한 날짜에 대한 메모 추가 및 이전 화면으로 전달

---


## 🛠 주요 화면 및 기능

### 1️⃣ ViewController (첫 번째 화면)
- UIDatePicker를 통해 약속 시간 선택
- 화면 전환 시 `prepare(for:sender:)`를 통해 다음 화면(ViewController2)에 날짜 문자열 전달
- 라이프사이클 로그 출력으로 상태 확인

### 2️⃣ ViewController2 (날짜 확인 화면)
- 전달받은 날짜를 Alert로 사용자에게 확인
- 사용자가 "Yes" 클릭 시 label에 "Good!!" 표시
- 사용자가 "No" 클릭 시 label에 "Oops!" 표시 및 이전 화면으로 돌아감
- 화면 전환 시 ViewController3에 날짜 문자열 전달

### 3️⃣ ViewController3 (메모 입력 화면)
- TextView를 통해 사용자가 날짜에 대한 메모 작성
- "Done" 버튼을 클릭하면 작성한 메모를 ViewController2에 전달
- 이전 화면으로 자동 복귀는 없음 (수동 처리 필요)

---


## 🧪 실행 방법

1. Xcode에서 `Scheduler.xcodeproj` 또는 `Scheduler.xcworkspace` 열기
2. 시뮬레이터 또는 실제 기기에서 실행
3. 첫 화면에서 날짜/시간을 선택하고 버튼을 클릭하여 다음 화면으로 이동
4. Alert에서 "Yes"/"No"를 눌러 결과 확인
5. 추가 메모를 입력하여 이전 화면에 반영

---


## 📂 디렉토리 구조
Scheduler/  
├── ViewController.swift // 첫 번째 화면: UIDatePicker  
├── ViewController2.swift // 두 번째 화면: 날짜 확인 및 Alert  
├── ViewController3.swift // 세 번째 화면: 메모 입력  
├── Main.storyboard // UI 구성  
├── Assets.xcassets // 앱 리소스  
└── Info.plist // 앱 설정  

---


## 📸 화면 예시

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/d1b12bb0-6126-4d8d-aa5f-dec160b1321f" width="200"/></td>
    <td><img src="https://github.com/user-attachments/assets/dab353d2-d2c0-475a-b387-7367eda242d8" width="200"/></td>
    <td><img src="https://github.com/user-attachments/assets/e1800f86-bc36-4c2e-8f63-6705712c3c73" width="200"/></td>
    <td><img src="https://github.com/user-attachments/assets/4fd98857-708a-4b80-986a-e68bb3a61df0" width="200"/></td>
  </tr>
</table>


---


## ✨ 학습 포인트

- `prepare(for:sender:)`를 통한 ViewController 간 데이터 전달
- UIAlertController 사용법 (ActionSheet 스타일)
- UINavigationController의 뷰 스택 구조 이해
- ViewController 라이프사이클 활용 (`viewWillAppear`, `viewDidDisappear` 등)
- AlertController의 handler 클로저 사용 예시 포함
- UINavigationController의 스택 인덱스를 활용하여 이전 화면 접근

