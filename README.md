
## EN

# DailyNihongo

**DailyNihongo** is an iOS Japanese learning app designed for Korean speakers.

Study Japanese vocabulary, kanji, and grammar from **JLPT N5 to N1** through structured learning stages, quizzes, and daily practice.

All learning content is bundled with the app as local JSON files. Learning lists, quizzes, Daily Word, and Lock Screen widgets work entirely offline. Learning progress and user preferences are stored locally on the device.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
  - [JLPT Learning](#jlpt-learning)
  - [Japanese Placement Test](#japanese-placement-test)
  - [Quizzes](#quizzes)
  - [Favorites](#favorites)
  - [Learning Records](#learning-records)
  - [Daily Learning](#daily-learning)
  - [Lock Screen Widget](#lock-screen-widget)
  - [Study Reminders and Appearance](#study-reminders-and-appearance)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Contact](#contact)

---

## Project Overview

DailyNihongo consists of four main tabs.

| Tab | Description |
| --- | --- |
| **Home** | Daily Word, Daily Grammar, monthly learning statistics, and favorites |
| **Learning** | JLPT-level vocabulary, kanji, and grammar learning, including mixed stage-based exercises |
| **Quiz** | Category-based quizzes, incorrect-answer reviews, and JLPT practice questions |
| **Records** | Learning calendar and quiz and stage-learning history |

On the first launch, users can take a **20-question Japanese placement test** to determine their recommended starting level.

Users can then study content for their selected JLPT level through structured learning stages or browse the complete content list, followed by quizzes using the same learning data.

### Bundled Learning Data

| Category | N5 | N4 | N3 | N2 | N1 | Total |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Vocabulary | 674 | 630 | 1,659 | 1,778 | 3,070 | **7,811** |
| Kanji | 84 | 169 | 387 | 398 | 1,345 | **2,383** |
| Grammar | 81 | 98 | 101 | 123 | 123 | **526** |
| **Total** | **839** | **897** | **2,147** | **2,299** | **4,538** | **10,720** |

---

## Key Features

### JLPT Learning

- **Vocabulary (N1–N5)**
  - Browse vocabulary by JLPT level.
  - View written forms, readings, meanings, and example sentences.
  - Search by word, reading, or meaning.

- **Kanji (N1–N5)**
  - Explore kanji with on'yomi, kun'yomi, meanings, stroke counts, and related vocabulary.
  - Search by character, meaning, or reading.

- **Grammar (N1–N5)**
  - Study grammar patterns, meanings, connection forms, example sentences, and additional notes.
  - Search by grammar pattern, meaning, reading, connection form, romaji, or notes.

- **Stage-based Learning**
  - Study vocabulary and kanji in groups of 20 items.
  - Study grammar in groups of 10 items.
  - Use flashcards to review each stage.
  - Completed stages are saved as learning progress.

- **Full Content List**
  - Browse all items for the selected JLPT level in one list.
  - Navigate between adjacent items from the detail screen.

### Japanese Placement Test

The app offers a **Japanese Placement Test** on the first launch.

- 20 questions in total.
- 2 vocabulary and 2 grammar questions for each JLPT level from N5 to N1.
- Recommends a learning level based on accuracy at each level.
- Users can start with the recommended level or manually select another level.
- The test can also be skipped.

### Quizzes

All quizzes use a four-choice multiple-choice format.

| Setting | Options |
| --- | --- |
| Question Count | 10, 20, 30, 50, 100, Unlimited |
| JLPT Range | Individual Level or All Levels |
| Time Limit | 5 or 10 seconds |
| Additional Options | Haptic Feedback, Consecutive Correct Answer Effects |

**Available Quiz Types**

- **Vocabulary Quiz**
  - Meaning recognition
  - Reading recognition
  - Word selection based on meaning
  - Example sentence fill-in-the-blank

- **Kanji Quiz**
  - Meaning recognition
  - On'yomi / Kun'yomi questions

- **Grammar Quiz**
  - Grammar pattern to meaning
  - Meaning to grammar pattern
  - Example sentence fill-in-the-blank

- **Incorrect Answer Review**
  - Retry incorrectly answered questions from vocabulary, kanji, and grammar quizzes.
  - Correctly answered questions are automatically removed from the review list.

- **Mixed Stage Quiz**
  - Combines kanji, vocabulary, and grammar questions from the same learning stage.
  - Uses the same stage sizes as flashcard learning.

- **JLPT Practice Questions**
  - 30 questions each for N1 and N2.
  - Covers kanji readings, contextual vocabulary, similar meanings, correct word usage, grammar, and sentence ordering.

> **Note:** Incorrect answers from Daily Word, Mixed Stage Quizzes, JLPT Practice Questions, and the Placement Test are not added to the incorrect answer review list.

### Favorites

- Bookmark vocabulary, kanji, and grammar using the star button.
- Revisit saved items by category through the Favorites section on the Home tab.

### Learning Records

The Records tab provides:

- Monthly learning calendar.
- Number of study days in the current month.
- Longest consecutive study streak.
- Question-level correct and incorrect answer history for vocabulary, kanji, and grammar quizzes.
- Daily Word learning history.
- Stage-based flashcard completion history.

Completing a stage-based flashcard session also counts as a study day.

### Daily Learning

- **Daily Word**
  - Opens a meaning-based quiz from the Home tab.
  - JLPT level selection: All or N1–N5.
  - Question count: 5, 10, 20, or 30.
  - Available once per day.
  - Displays the number of correct answers on the Home screen.

- **Daily Grammar**
  - Selects one grammar item per day based on the date.
  - Uses the JLPT level configured in Settings.
  - Opens the selected grammar item's detail screen.

### Lock Screen Widget

DailyNihongo provides a WidgetKit Lock Screen widget called **Daily Japanese**.

- Supports the rectangular accessory widget (`accessoryRectangular`).
- Displays either vocabulary or kanji.
- Vocabulary: Written form, reading, and meaning.
- Kanji: Character, on'yomi / kun'yomi, and meaning.
- JLPT level selection.
- Content type selection (Vocabulary / Kanji).
- Refresh intervals: 15, 20, 25, 30, 45, or 60 minutes.
- Default refresh interval: 30 minutes.
- Tapping the widget opens the corresponding vocabulary or kanji detail screen in the Learning tab.

### Study Reminders and Appearance

- **Study Reminders**
  - Recurring daily local notifications.
  - Customizable reminder time.
  - Default reminder time: 9:00 AM.

- **Appearance**
  - System
  - Light
  - Dark

- **Data Management**
  - Reset learning records.
  - Reset incorrect answers.
  - Reset favorites.
  - Reset Daily Word progress.
  - Reset all user data.
  - Bundled learning JSON files are preserved when user data is reset.

---

## Tech Stack

| Category | Technology |
| --- | --- |
| Language | Swift 5 |
| UI Framework | SwiftUI |
| Architecture | Feature-based MVVM |
| Development Environment | Xcode 26.2 |
| Deployment Target | iOS 18.6+ |
| Platform | iPhone |
| Learning Data | Local JSON |
| User Data Storage | UserDefaults |
| Widget Settings | App Group UserDefaults |
| Widgets | WidgetKit |
| Notifications | UserNotifications |
| Version Control | Git / GitHub |

The project has **no external Swift Package dependencies**.

**Current Version:** `1.2.1`

---

## Project Structure

```text
DailyNihongo/
├── DailyNihongo.xcodeproj
├── DailyNihongo/
│   ├── App/
│   ├── Core/
│   │   ├── Components/
│   │   ├── Services/
│   │   ├── Theme/
│   │   └── Utilities/
│   ├── Data/
│   │   ├── Models/
│   │   └── Stores/
│   ├── Features/
│   │   ├── Home/
│   │   ├── Learning/
│   │   ├── Vocabulary/
│   │   ├── Kanji/
│   │   ├── Grammar/
│   │   ├── Quiz/
│   │   ├── Placement/
│   │   ├── DailyWord/
│   │   ├── Favorites/
│   │   ├── StudyRecord/
│   │   └── Settings/
│   ├── Resources/
│   └── Shared/
└── DailyNihongoWidget/
```

| Directory | Description |
| --- | --- |
| `App` | App entry point (`@main`), main tabs, appearance configuration, and widget URL handling |
| `Core/Components` | Shared UI components |
| `Core/Services` | Daily study reminder scheduling and notification permissions |
| `Core/Theme` | App colors and styling |
| `Core/Utilities` | Storage keys and study date calculations |
| `Data/Models` | Learning records, incorrect answers, stages, and JLPT practice question models |
| `Data/Stores` | User learning progress persistence using `UserDefaults` |
| `Features` | Feature-specific Views and ViewModels |
| `Resources` | Offline learning content in JSON format |
| `Shared` | Shared data repository, vocabulary, kanji, grammar models, and widget settings |
| `DailyNihongoWidget` | Lock Screen widget timeline and UI |

---

## Getting Started

### Requirements

- Xcode 26.2 or later
- iOS 18.6 or later
- iPhone Simulator or physical iPhone

---

## Contact

If you encounter any issues while using the app, feel free to contact us.

- **Email:** dailynihongo2026@gmail.com

When reporting an issue, please include your device model, iOS version, and app version to help us investigate more efficiently.


## KR
# DailyNihongo

DailyNihongo는 한국어 사용자를 위한 iOS 일본어 학습 앱입니다. JLPT N5부터 N1까지 단어, 한자, 문법을 단계로 나누어 익히고, 퀴즈와 매일 학습으로 복습합니다.
학습 콘텐츠는 앱에 포함된 JSON으로 제공됩니다. 학습 목록, 퀴즈, 오늘의 단어, 잠금 화면 위젯은 네트워크 없이 동작하며, 진행 상황과 설정은 기기에 저장됩니다.

## 프로젝트 개요
앱은 네 개의 탭으로 구성됩니다.
| 탭 | 역할 |
| --- | --- |
| 홈 | 오늘의 단어, 오늘의 문법, 이번 달 학습 현황, 즐겨찾기 |
| 학습 | JLPT 레벨별 한자·단어·문법 학습과 단계별 혼합 문제 |
| 퀴즈 | 영역별 퀴즈, 오답 복습, JLPT 연습문제 |
| 기록 | 학습 달력과 퀴즈·단계 학습 기록 |
처음 실행하면 20문항의 일본어 레벨 테스트로 시작 레벨을 정합니다. 이후에는 선택한 JLPT 레벨의 콘텐츠를 단계 학습과 전체 목록으로 공부하고, 같은 데이터를 퀴즈로 다시 확인합니다.

번들에 포함된 학습 데이터는 다음과 같습니다.
| 영역 | N5 | N4 | N3 | N2 | N1 | 합계 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| 단어 | 674 | 630 | 1,659 | 1,778 | 3,070 | 7,811 |
| 한자 | 84 | 169 | 387 | 398 | 1,345 | 2,383 |
| 문법 | 81 | 98 | 101 | 123 | 123 | 526 |

## 주요 기능

### JLPT 학습
- **단어 (N1–N5):** 표기, 읽기, 뜻, 예문을 레벨별 목록과 상세 화면에서 확인합니다. 표기·읽기·뜻으로 검색할 수 있습니다.
- **한자 (N1–N5):** 음독, 훈독, 뜻, 획수, 관련 단어를 확인합니다. 글자·뜻·읽기로 검색할 수 있습니다.
- **문법 (N1–N5):** 문형, 의미, 접속 형태, 예문, 보충 설명을 확인합니다. 문형·뜻·읽기·접속 형태·로마자·노트로 검색할 수 있습니다.
- **단계 학습:** 단어와 한자는 20개, 문법은 10개 단위로 나누어 플래시카드로 학습합니다. 마친 단계는 진행 상태로 저장됩니다.
- **전체 목록:** 선택 레벨의 항목을 한 목록에서 보고, 상세 화면에서 앞뒤 항목으로 이동합니다.

### 레벨 테스트
첫 실행 시 **일본어 레벨 테스트**를 진행합니다. N5에서 N1까지 단어 2문항, 문법 2문항씩 총 20문항이며, 레벨별 정답률로 추천 학습 레벨을 제시합니다. 추천 레벨로 시작하거나 다른 레벨을 직접 고를 수 있고, 테스트를 건너뛸 수도 있습니다.

### 퀴즈
퀴즈는 4지선다이며, 문항 수는 10·20·30·50·100·무제한 중에서 고릅니다. 범위는 한 JLPT 레벨 또는 전체입니다. 제한 시간(5초·10초), 햅틱, 연속 정답 효과를 설정에서 켤 수 있습니다.
- **단어 퀴즈:** 뜻, 읽기, 뜻에서 단어 찾기, 예문 빈칸.
- **한자 퀴즈:** 뜻, 음독·훈독.
- **문법 퀴즈:** 문형에서 의미, 의미에서 문형, 예문 빈칸.
- **오답 복습:** 단어·한자·문법 퀴즈에서 틀린 문제만 다시 풉니다. 맞힌 문제는 복습 목록에서 빠집니다.
- **단계별 혼합 퀴즈:** 학습 탭에서 같은 단계의 한자, 단어, 문법을 섞어 풉니다. 단계 크기는 플래시카드와 같습니다.
- **JLPT 연습문제:** N1·N2 각 30문항입니다. 한자 읽기, 문맥 어휘, 비슷한 의미, 올바른 용법, 문법, 문장 배열을 포함합니다.
오늘의 단어, 단계별 혼합 퀴즈, JLPT 연습문제, 레벨 테스트의 오답은 오답 복습 목록에 들어가지 않습니다.

### 즐겨찾기
단어, 한자, 문법에 별표를 남기고 홈의 즐겨찾기에서 영역별로 다시 볼 수 있습니다.

### 학습 기록
기록 탭은 월별 달력, 그달의 학습일 수, 최장 연속 학습일을 보여 줍니다. 단어·한자·문법 퀴즈와 오늘의 단어는 문항별 정오답까지 저장됩니다. 단계 플래시카드를 끝낸 날도 학습일에 포함됩니다.

### 매일 학습
- **오늘의 단어:** 홈에서 뜻 맞히기 퀴즈를 엽니다. 레벨은 전체 또는 N1–N5, 문항 수는 5·10·20·30입니다. 하루에 한 번 풀며, 정답 수를 홈에 표시합니다.
- **오늘의 문법:** 설정한 레벨에서 날짜에 따라 문법 하나를 골라 상세 화면으로 엽니다.

### 잠금 화면 위젯
WidgetKit 잠금 화면 위젯 **오늘의 일본어**를 제공합니다. 직사각형 액세서리(`accessoryRectangular`)에 단어 또는 한자를 표시합니다.
- 단어는 표기, 읽기, 뜻을 보여주고, 한자는 글자, 음독·훈독, 뜻을 보여 줍니다.
- JLPT 레벨, 콘텐츠 종류(단어/한자), 갱신 간격(15·20·25·30·45·60분, 기본 30분)을 설정할 수 있습니다.
- 위젯을 누르면 앱의 학습 탭에서 해당 단어 또는 한자 상세로 이동합니다.

### 학습 알림과 화면 모드
- **학습 알림:** 지정한 시각에 매일 반복되는 로컬 알림을 보냅니다. 기본 시각은 오전 9시입니다.
- **화면 모드:** 자동(시스템), 라이트, 다크 중에서 고릅니다.
- **데이터 관리:** 학습 기록, 오답, 즐겨찾기, 오늘의 단어 진행, 또는 사용자 데이터 전체를 초기화할 수 있습니다. 앱에 포함된 학습 JSON은 유지됩니다.

## 기술 스택
| 항목 | 내용 |
| --- | --- |
| 언어 | Swift 5 |
| UI | SwiftUI |
| 구조 | 기능 단위 MVVM. 화면은 `Features`의 View와 `ObservableObject` ViewModel이 담당합니다. |
| 개발 환경 | Xcode 26.2 |
| 배포 대상 | iOS 18.6 이상, iPhone |
| 학습 데이터 | 앱 번들의 로컬 JSON |
| 사용자 데이터 | `UserDefaults`. 퀴즈 기록, 오답, 단계 학습 기록은 JSON으로 인코딩해 저장합니다. |
| 위젯 설정 | App Group `UserDefaults` |
| 위젯 | WidgetKit |
| 알림 | UserNotifications 로컬 알림 |
| 버전 관리 | Git, GitHub |
외부 Swift 패키지 의존성은 없습니다. 현재 버전은 1.2.1입니다.

## 프로젝트 구조
```
DailyNihongo/
├── DailyNihongo.xcodeproj
├── DailyNihongo/
│   ├── App/                 # 앱 진입, 탭, 위젯 딥링크
│   ├── Core/
│   │   ├── Components/      # 검색, 레벨 선택, 즐겨찾기 등 공통 UI
│   │   ├── Services/        # 로컬 알림
│   │   ├── Theme/           # 색상
│   │   └── Utilities/       # UserDefaults 키, 학습일 계산
│   ├── Data/
│   │   ├── Models/          # 학습 기록, 오답, 연습 문제 모델
│   │   └── Stores/          # 기록·오답·진행 상태 저장
│   ├── Features/
│   │   ├── Home/            # 홈
│   │   ├── Learning/        # 단계 학습, 플래시카드
│   │   ├── Vocabulary/      # 단어
│   │   ├── Kanji/           # 한자
│   │   ├── Grammar/         # 문법
│   │   ├── Quiz/            # 단어·한자·문법·단계·오답·JLPT 연습
│   │   ├── Placement/       # 레벨 테스트
│   │   ├── DailyWord/       # 오늘의 단어
│   │   ├── Favorites/       # 즐겨찾기
│   │   ├── StudyRecord/     # 학습 기록
│   │   └── Settings/        # 설정
│   ├── Resources/           # 단어·한자·문법·연습·레벨 테스트 JSON
│   └── Shared/              # 앱과 위젯이 함께 쓰는 데이터 로더와 모델
└── DailyNihongoWidget/      # 잠금 화면 위젯
```
| 디렉터리 | 역할 |
| --- | --- |
| `App` | `@main` 진입점, 네 개 탭, 화면 모드 적용, 위젯 URL 처리 |
| `Data/Models` | 학습 기록, 오답, 단계, JLPT 연습 문제 모델 |
| `Data/Stores` | 사용자 진행 데이터를 `UserDefaults`에 읽고 씁니다. |
| `Features` | 화면과 해당 화면의 ViewModel. 퀴즈·학습·설정 등 기능별로 나뉩니다. |
| `Core/Services` | 매일 학습 알림 예약과 권한 처리 |
| `Core/Utilities` | 저장 키와 학습일·연속 학습 계산 |
| `Resources` | 오프라인 학습 JSON |
| `Shared` | `JapaneseDataRepository`와 단어·한자·문법 모델, 위젯 설정 |
| `DailyNihongoWidget` | 잠금 화면 타임라인과 위젯 UI |

## 실행
Xcode 26.2 이상에서 `DailyNihongo.xcodeproj`를 열고, iOS 18.6 이상 iPhone 시뮬레이터 또는 기기에서 앱 타깃을 실행합니다.

## 문의

앱 사용 중 문제가 있으면 이메일로 연락해 주세요.

- 이메일: dailynihongo2026@gmail.com

기기 기종, iOS 버전, 앱 버전을 함께 적어 주시면 확인이 더 빠릅니다.
