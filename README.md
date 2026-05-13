# Dramatis Personae · The Gospel of Mark

마가복음에 등장하는 30인의 캐릭터 시트를 그리드 + 줌 가능한 시트 뷰어로 보여주는 정적 사이트입니다.

## 구조

```
mark-personae/
├── index.html          단일 페이지 (모든 코드 포함)
├── images/             30장의 캐릭터 시트 (JPG)
│   ├── 01-jesus.jpg
│   ├── 02-john-baptist.jpg
│   ├── ...
│   └── 30-joseph-arimathea.jpg
└── README.md
```

총 용량: 약 10 MB.

## 인터랙션

- **그리드 → 시트 뷰**: 카드를 누르면 풀스크린 뷰어
- **줌**: 마우스 휠 / 핀치 / `+` `−` 버튼 / `+` `−` 키
- **팬**: 드래그 / 1손가락 터치
- **네비**: 좌우 화살표 키, 화면 양쪽 버튼
- **맞춤 복귀**: 더블클릭/탭, `0` 키, ⤾ 버튼
- **설명 토글**: `i` 키 또는 ⓘ 버튼 (각 인물의 짧은 노트 + 인용구)
- **닫기**: `Esc` 키, × 버튼
- **딥링크**: `?p=jesus` 같은 URL로 특정 인물 시트 직접 공유

## GitHub Pages 배포

### 1. 새 repo 생성
GitHub에서 `mark-personae` (또는 원하는 이름) 으로 public repo를 만듭니다.

### 2. 파일 푸시
이 폴더 그대로 푸시하면 됩니다.
```bash
cd mark-personae
git init
git add .
git commit -m "Initial: 30 character sheets"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/mark-personae.git
git push -u origin main
```

### 3. Pages 활성화
GitHub repo → **Settings → Pages**
- **Source**: Deploy from a branch
- **Branch**: `main` / `(root)`
- **Save**

약 1분 후 `https://<YOUR_USERNAME>.github.io/mark-personae/` 로 접속 가능합니다.

### 4. (선택) 커스텀 도메인
**Settings → Pages → Custom domain** 에 도메인 입력. DNS는 GitHub Pages 가이드 참고.

## 대안 호스팅

- **Netlify Drop**: https://app.netlify.com/drop 에 이 폴더 통째로 드래그
- **Vercel**: `vercel deploy` (Vercel CLI)
- **로컬 미리보기**: `python3 -m http.server 8000` 후 `http://localhost:8000`

## 인물 명단 (마가복음 등장 순)

| # | English | 한글 | 등장 |
|---|---|---|---|
| 01 | Jesus Christ | 예수 그리스도 | 1:1 |
| 02 | John the Baptist | 세례 요한 | 1:4 |
| 03 | Simon Peter | 시몬 베드로 | 1:16 |
| 04 | James (Zebedee) | 야고보 (세베대의 아들) | 1:19 |
| 05 | John (Zebedee) | 요한 (세베대의 아들) | 1:19 |
| 06 | The Capernaum Demoniac | 가버나움 귀신들린 자 | 1:23 |
| 07 | Peter's Mother-in-law | 시몬 베드로의 장모 | 1:30 |
| 08 | The Leper | 나병환자 | 1:40 |
| 09 | The Paralytic | 중풍병자 | 2:3 |
| 10 | Matthew (Levi) | 마태 (레위) | 2:14 |
| 11 | Jairus | 회당장 야이로 | 5:22 |
| 12 | The Hemorrhaging Woman | 혈루병 걸린 여인 | 5:25 |
| 13 | Jairus's Daughter | 야이로의 딸 | 5:35 |
| 14 | Herod Antipas | 헤롯 안디바스 | 6:14 |
| 15 | Herodias | 헤로디아 | 6:17 |
| 16 | Salome | 살로메 (헤로디아의 딸) | 6:22 |
| 17 | The Syrophoenician Woman | 수로보니게 여인 | 7:26 |
| 18 | Moses | 모세 (변화산) | 9:4 |
| 19 | Elijah | 엘리야 (변화산) | 9:4 |
| 20 | Bartimaeus | 바디매오 | 10:46 |
| 21 | The Anointing Woman | 향유 부은 여인 | 14:3 |
| 22 | Judas Iscariot | 가룟 유다 | 14:10 |
| 23 | Caiaphas | 대제사장 가야바 | 14:53 |
| 24 | Sanhedrin Member | 산헤드린 의원 | 14:55 |
| 25 | Pontius Pilate | 총독 빌라도 | 15:1 |
| 26 | Barabbas | 바라바 | 15:7 |
| 27 | Simon of Cyrene | 구레네 사람 시몬 | 15:21 |
| 28 | The Centurion | 로마 백부장 | 15:39 |
| 29 | Mary Magdalene | 막달라 마리아 | 15:40 |
| 30 | Joseph of Arimathea | 아리마대 요셉 | 15:43 |

## 인물 수정·교체

각 인물 정보는 `index.html` 안 `const characters = [...]` 배열에서 직접 편집할 수 있습니다.
이미지를 교체할 땐 `images/` 폴더의 해당 파일을 같은 이름으로 덮어쓰면 됩니다 (파일명 유지가 핵심).

캐릭터 시트는 1세기 유대·로마 문화를 기반으로 한 시각적 추정입니다.
