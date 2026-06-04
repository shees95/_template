# 🚀 프로젝트 초기 설정 가이드

## 📄 1. 템플릿 레포지토리 생성

GitHub의 `_Template` 레포지토리를 기반으로 새로운 프로젝트를 생성합니다.

1. GitHub에서 `_Template` 선택
2. **Use this template** 클릭
3. 새로운 Repository 생성

---

## 🖨️ 2. Repository 클론
기존 원격 저장소 연결 확인

```bash
git remote -v
```

예상 결과

```bash
origin  https://github.com/shees95/_template.git (fetch)
origin  https://github.com/shees95/_template.git (push)
```



기존 원격 저장소 삭제, 새 원격 저장소 연결
```bash
git remote remove origin
git remote add origin https://github.com/아이디/레포명.git
```

원격 저장소 연결 확인

```bash
git remote -v
```

예상 결과

```bash
origin  https://github.com/아이디/레포명.git (fetch)
origin  https://github.com/아이디/레포명.git (push)
```

---

## 📝 3. 프로젝트명 변경

프로젝트명에 맞게 디렉토리 및 설정 파일을 수정합니다.

```text
_Template
    ↓
프로젝트명
```

확인 항목

* 솔루션(.sln) 이름
* 프로젝트(.uproject) 이름
* 폴더 이름
* README 제목

---

## 🚫 4. .gitignore / .gitattributes 설정

프로젝트 유형에 맞는 설정 파일을 선택합니다.

### C++ 프로젝트

```text
cpp.gitignore
    ↓
.gitignore
```

### Unreal Engine 프로젝트

```text
unreal.gitignore
    ↓
.gitignore
```

### Git LFS 사용 시

필요한 `.gitattributes` 파일의 이름을 변경합니다.

```text
unreal.gitattributes
    ↓
.gitattributes
```

---

### 적용 예시

```bash
ren unreal.gitignore .gitignore
ren unreal.gitattributes .gitattributes
```

또는

```bash
mv unreal.gitignore .gitignore
mv unreal.gitattributes .gitattributes
```

---

### 확인

```bash
git status
```

`.gitignore`, `.gitattributes` 파일이 정상적으로 적용되었는지 확인합니다.


---

## ✅ 5. 초기 상태 확인

```bash
git status
```

변경 사항 확인 후

```bash
git add .
git commit -m "Init Project"
git push origin main
```

---

## 🎯 체크리스트

* [ ] 템플릿 레포지토리 생성
* [ ] 프로젝트 클론
* [ ] 원격 저장소 확인
* [ ] 프로젝트명 변경
* [ ] .gitignore 설정
* [ ] .gitattributes 설정
* [ ] 초기 커밋 및 Push
