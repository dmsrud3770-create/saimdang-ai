# 업무 PC — Claude Code 연동 가이드
> 이 순서대로 따라하면 메인 PC와 동일하게 사용 가능

---

## STEP 1. Claude Code 설치

업무 PC에서 **PowerShell** 열기
(윈도우 시작 → "PowerShell" 검색 → 실행)

아래 명령어 복사해서 붙여넣고 엔터:

```
irm https://claude.ai/install.ps1 | iex
```

설치 완료 확인:
```
claude --version
```

---

## STEP 2. 로그인

PowerShell에서 실행:
```
claude
```

→ 브라우저 자동 열림
→ **지금 메인 PC에서 쓰는 동일한 Anthropic 계정**으로 로그인
→ "승인" 클릭하면 자동 연결됨

---

## STEP 3. 프로젝트 폴더 연동

### ✅ 추천 방법 — OneDrive 사용

메인 PC에서:
1. `C:\Users\User\클로드코드` 폴더를
2. OneDrive 폴더 안으로 이동 (잘라내기 → 붙여넣기)

업무 PC에서:
```
cd "C:\Users\[업무PC 계정명]\OneDrive\클로드코드"
claude
```

→ 자동 동기화되어 항상 최신 파일 유지

---

### 다른 방법 — USB 복사

1. 메인 PC의 `클로드코드` 폴더를 USB에 복사
2. 업무 PC 원하는 위치에 붙여넣기
3. PowerShell에서:
```
cd "C:\Users\[업무PC 계정명]\클로드코드"
claude
```

---

## STEP 4. 설정 파일 복사

메인 PC에서 이 파일을:
```
C:\Users\User\AppData\Roaming\Claude\settings.json
```

USB 또는 OneDrive로 업무 PC 동일 경로에 복사:
```
C:\Users\[업무PC 계정명]\AppData\Roaming\Claude\settings.json
```

> AppData 폴더가 안 보이면:
> 파일 탐색기 → 보기 → 숨긴 항목 체크

---

## STEP 5. 첫 실행 및 권한 승인

```
claude
```

→ 권한 요청 팝업이 뜨면 **Allow (허용)** 클릭
→ 완료!

---

## ✅ 최종 체크리스트

- [ ] STEP 1 — Claude Code 설치
- [ ] STEP 2 — 동일 계정 로그인
- [ ] STEP 3 — 프로젝트 폴더 연동 (OneDrive 추천)
- [ ] STEP 4 — settings.json 복사
- [ ] STEP 5 — 권한 승인 후 사용 시작

---

## 막히면?

자비스한테 바로 물어보세요!
"자비스, 업무 PC 연동하다가 [문제] 나왔어" 라고 하면 바로 도와드려요.
