# RITA Codespace

RITA Codespace는 수업에서 진행되는 학생 프로젝트를 등록하고 공유하기 위한 GitHub Organization입니다.

학생들은 각자의 Repository에 프로젝트 결과물을 업로드하고, 다른 학생들의 작업을 자유롭게 열람할 수 있습니다.

Organization에 가입할 필요는 없습니다. **GitHub 계정만 있으면** 아래 절차로 본인 프로젝트 Repository를 바로 만들 수 있습니다 (계정당 최대 5개).

---

## 🚀 Getting Started: 프로젝트 등록 방법

> **등록 링크:** https://github.com/rita-codespace/submissions/issues/new/choose

1. 본인의 **GitHub 계정으로 로그인**합니다. 계정이 없다면 [github.com/signup](https://github.com/signup)에서 먼저 만드세요.
2. 위 **등록 링크**에 접속합니다.
3. **Project Repository Registration** 양식을 선택하고(New Issue), **프로젝트명**, **저장소 이름**(영문 소문자·숫자·하이픈), **프로젝트 간단 설명**을 적은 뒤 확인란을 체크하고 **Create**를 누릅니다.
4. 별도 승인 없이 1~2분 안에 Repository `rita-codespace/<본인 GitHub ID>-<저장소 이름>`이 **자동으로 생성**되고, 결과가 Issue 댓글로 안내됩니다.
5. 댓글의 초대 링크(또는 GitHub 알림·이메일)에서 **Collaborator 초대를 수락(Accept invitation)** 합니다.
6. 생성된 Repository에 본인의 프로젝트를 **업로드**합니다. 방법은 아래 [코드 업로드 방법](#코드-업로드-방법)을 참고하세요.

<details>
<summary>등록 시 자주 묻는 질문</summary>

- **GitHub ID를 입력해야 하나요?** 아니요. Issue를 작성한 계정에서 자동으로 확인합니다. 다른 사람 대신 등록할 수는 없습니다.
- **여러 개 만들 수 있나요?** 네. 프로젝트마다 저장소 이름을 다르게 적어 등록하면 계정당 최대 5개까지 만들 수 있습니다. 같은 이름으로 다시 등록하면 새로 만들지 않고 기존 Repository를 안내합니다.
- **초대가 만료됐어요.** 초대는 7일 후 만료됩니다. **같은 저장소 이름**으로 등록 양식을 다시 제출하면 새 초대가 발송됩니다.
- **GitHub 아이디를 바꿨어요.** 기존 Repository는 그대로 본인 것으로 인식됩니다. 같은 저장소 이름으로 다시 등록해도 새로 만들어지지 않고 기존 Repository가 안내됩니다.
- **댓글에 ⚠️ 안내가 달렸어요.** 저장소 이름 형식이 맞지 않거나 5개 한도를 넘은 경우입니다. 안내대로 고쳐 새 등록 Issue를 작성하세요.
- **댓글에 ❌ 오류가 달렸어요.** 시스템 문제이므로 관리자가 확인한 뒤 처리합니다. Issue를 지우지 말고 기다려 주세요.

</details>

---

## 🗂️ Repository Structure

```
rita-codespace/
├── submissions             ← 등록 접수처 (Issue로 Repository 생성 신청)
├── studentA-smart-campus   ← 학생 A의 프로젝트
├── studentA-chatbot        ← 학생 A의 두 번째 프로젝트
└── studentB-smart-campus   ← 학생 B의 프로젝트
```

- 학생 Repository 이름은 `<GitHub ID>-<저장소 이름>` 형식입니다. 저장소 이름은 등록할 때 직접 정합니다 (영문 소문자·숫자·하이픈, 2~40자).
- 각 학생은 **본인 Repository에 대한 수정(Write) 권한**을 받습니다.
- `submissions`는 등록 신청 전용입니다. 이곳에 코드를 올리지 마세요.

---

## 📦 Submission Guidelines

### 코드 업로드 방법

초대를 수락한 뒤 아래 방법 중 하나로 업로드합니다.

**Git 명령어 사용**

```bash
git clone https://github.com/rita-codespace/<본인 GitHub ID>-<저장소 이름>.git
cd <본인 GitHub ID>-<저장소 이름>

# 프로젝트 파일을 이 폴더에 넣은 뒤
git add .
git commit -m "Add project source"
git push
```

**웹에서 업로드**

Repository 페이지에서 **Add file → Upload files**를 눌러 파일을 끌어다 놓고 **Commit changes**를 누릅니다.

> 업로드 전에 `.env`, 키 파일, `node_modules`처럼 올리면 안 되거나 불필요한 파일이 포함되지 않았는지 확인하세요. `.gitignore`를 사용하면 편리합니다.

### README 작성 안내

Repository 최상위의 `README.md`는 다른 사람이 프로젝트를 이해하는 첫 화면입니다. 아래 항목은 **권장 작성 항목**이며, 현재 필수 제출 요건은 아닙니다.

| 항목 | 작성 내용 |
|---|---|
| Project Title | 프로젝트 이름 |
| Team Members | 참여 구성원과 역할 |
| Project Description | 프로젝트의 목적과 배경 |
| Main Features | 주요 기능 |
| Technical Stack | 사용한 언어, 프레임워크, 라이브러리 |
| Architecture | 시스템 구조 (간단한 다이어그램 또는 설명) |
| How to Run | 설치 및 실행 방법 |
| Screenshots | 실행 화면 (해당하는 경우) |

### 평가·제출 규정 (Course Requirements)

> 교수님이 정하는 실제 평가 및 제출 규정이 이곳에 추가될 예정입니다. **TBA (추후 공지)**

---

## 🛡️ Repository Policy

- 학생은 **본인의 Repository를 직접 수정**할 수 있습니다.
- **다른 학생의 Repository는 자유롭게 열람**할 수 있습니다.
- 다른 학생의 Repository를 **직접 수정하거나 삭제할 권한은 제공되지 않습니다.**
- Repository는 기본적으로 **Public**으로 공개됩니다.
- **API Key, Password, Access Token** 등의 민감정보를 업로드해서는 안 됩니다. 실수로 올렸다면 해당 키를 즉시 폐기(재발급)하세요. 커밋을 지워도 기록이 남을 수 있습니다.
- **저작권을 침해**하거나 **공개에 부적절한** 코드·자료를 업로드해서는 안 됩니다.
- Repository 삭제, 이름 변경, 공개 범위 변경, Collaborator 추가는 관리자만 할 수 있습니다.
- 관리자는 운영상 문제가 있는 Repository를 관리(수정·비공개·삭제)할 수 있습니다.

---

## 📅 Important Dates

| 항목 | 내용 |
|---|---|
| Registration Period | TBA (추후 공지) |
| Submission Deadline | TBA (추후 공지) |
| Required Deliverables | TBA (추후 공지) |
| Additional Instructions | TBA (추후 공지) |

---

## 💬 Contact & Support

Repository 자동 생성이나 권한 문제가 발생하면 아래 방법으로 문의하세요.

- 등록 Issue에 달린 **댓글을 먼저 확인**하세요. ⚠️ 안내는 내용을 고쳐 다시 신청하면 되고, ❌ 오류는 관리자가 해당 Issue를 보고 처리합니다.
- 그 밖의 문의는 [`submissions`의 **문의 (Question / Support)** 양식](https://github.com/rita-codespace/submissions/issues/new?template=question.yml) 또는 **수업에서 안내된 공식 채널**을 이용하세요.
