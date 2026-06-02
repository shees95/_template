# 🚀 프로젝트 초기 설정 가이드

## 📄 1. 템플릿 레포지토리 생성

GitHub의 `_Template` 레포지토리를 기반으로 새로운 프로젝트를 생성합니다.

1. GitHub에서 `_Template` 선택
2. **Use this template** 클릭
3. 새로운 Repository 생성

---

## 🖨️ 2. Repository 클론

```bash
git clone https://github.com/아이디/레포명.git
cd 레포명
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

프로젝트 환경에 맞는 Git 설정을 적용합니다.

### .gitignore

버전 관리가 필요 없는 파일 제외

예시

```text
Binaries/
Intermediate/
Saved/
DerivedDataCache/
.vs/
```

### .gitattributes

Git LFS 및 텍스트 처리 설정

예시

```text
*.uasset filter=lfs diff=lfs merge=lfs -text
*.umap   filter=lfs diff=lfs merge=lfs -text
```

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
