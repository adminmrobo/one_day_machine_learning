# 「하루에 다 끝내는 머신러닝 서머리 노트 — 오전반」 이미지 제작 명세서

- 페이지: `index.html` (단일 파일) · 분야: 인공지능 · 형식: 미션형(쪽지시험 대비, 대결 없음) · 주 앵커: 생활·현장(시험 공부)
- 대결 없음 — 아웃트로 표정: 박사 `doc_e16`, 초파리 `fly_e09`, 주판봇 `robo_e09`, 시아 `sia_e17`(졸음), 모아 `moa_e12`, 조수 `asst_e16`
- 만든 날: 2026-11-13 · 캐릭터 팩 1.4 (`fruitfly-lab-expressions` @ 86d04ac)

## 1. 그림체와 고정 외형
캐릭터 팩 `CHAR_lab4.md` 18-3·18-4 그대로. 16비트 RPG풍 픽셀아트, 굵은 어두운 외곽선, 밤의 연구실 조명. 그림 안에 글자·숫자·로고를 넣지 않습니다. 로봇은 주판봇(베이지 상자형)만 씁니다.

## 2. 필요한 그림 전체

| 키 | 판 | 쓰는 자리 | 상태 | 비고 |
|---|---|---|---|---|
| `cover_one_day_ml_am` | L 1920×1080 | 페이지 맨 위 표지 | **새로 그림** | 지금은 대체 표지(칠판 시간표 + 캐릭터 여섯). 지시문 `COVER_one_day_ml_am.md` |
| `og_one_day_ml_am` | K 1200×630 | 공유 미리보기 | 표지에서 자름 | 표지 반영 때 `og:image` 메타 추가 |
| `thumb_one_day_ml_am` | I 600×400 | 목차·현황판 썸네일 | 표지에서 자름 | |
| `sc_period1` | E 1200×800 | 1교시 머리 장면 | 새로 그림 · 선택 | 지금은 코드로 그린 칠판 장면 |
| `sc_period2` | E 1200×800 | 2교시 머리 장면 | 새로 그림 · 선택 | 〃 |
| `sc_period3` | E 1200×800 | 3교시 머리 장면 | 새로 그림 · 선택 | 〃 |
| `sc_period4` | E 1200×800 | 4교시 머리 장면 | 새로 그림 · 선택 | 〃 |
| 표정 37장 | A~D | 말풍선·대화·식구 카드·암기 카드 | **캐릭터 팩 재사용** | 아래 4번 목록. 새로 그릴 것 없음 |

만드는 순서: ① 표지 → 그림체 확인 → ② 교시 장면 네 장(같은 대화에서, 표지를 참고 그림으로 함께 올림).

## 3. 새로 그릴 그림 상세

### 3-1. `cover_one_day_ml_am` — 시험 전날의 공부 책상
`COVER_one_day_ml_am.md`의 프롬프트를 그대로 씁니다. 반영: 1600×900 WebP 220 KB 이하, `alt`는 지시문의 대체 글.

### 3-2. 교시 장면 네 장 (선택)
공통 머리말을 붙이고 장면 문장만 바꿉니다.

```
Wide 3:2 scene, 16-bit RPG style pixel art matching the attached reference images and the attached cover, thick dark outlines, night research lab with purple light and a warm desk lamp. Keep every character design exactly as in the references. No text, no letters, no numbers, no logos, no real brands.
Scene: {장면}
```

| 키 | {장면} | 대체 글 |
|---|---|---|
| `sc_period1` | The black-haired maid intern and the beige-haired maid intern sit at a study desk sorting two piles of cards: one pile has small answer tags attached, the other has none. The chibi scientist watches from behind with a thinking pose; the pink-haired researcher stands beside them. A sealed box sits on a shelf, tied with a ribbon. | 시아와 모아가 답표가 붙은 카드와 붙지 않은 카드를 두 더미로 나누고, 박사와 조수가 지켜봅니다. 선반에는 봉인한 상자가 있습니다 |
| `sc_period2` | The beige-haired maid intern wipes a large table of blank tiles with a cloth so that empty tiles fill in, while the black-haired maid intern dusts away one oversized tile with a feather duster. The boxy beige CRT robot counts tiles on a wooden abacus; the fruit fly researcher drinks coffee and watches. | 모아가 걸레로 빈칸을 채우고 시아가 먼지떨이로 튀는 타일 하나를 털어 냅니다. 주판봇이 주판으로 세고 초파리 연구원이 지켜봅니다 |
| `sc_period3` | The black-haired maid intern holds a long ruler against glowing dots floating above the desk, trying to line it up; the beige-haired maid intern points at one dot far away from the others with sparkling eyes. The pink-haired researcher explains with one hand raised; the boxy beige CRT robot holds its abacus. | 시아가 떠 있는 점들에 긴 자를 대어 보고, 모아가 멀리 떨어진 점 하나를 가리킵니다. 조수가 설명하고 주판봇이 주판을 듭니다 |
| `sc_period4` | Glowing green circles and red triangles float in two loose groups above the desk. The beige-haired maid intern cheers and stretches a ribbon between the two groups like a road; the black-haired maid intern is yawning, half asleep on her notebook. The fruit fly researcher points at one triangle hiding among the circles; the pink-haired researcher smiles. | 초록 동그라미와 빨간 세모 무리 사이에 모아가 리본으로 길을 냅니다. 시아는 공책 위에서 하품하고, 초파리 연구원이 동그라미 속에 숨은 세모 하나를 가리킵니다 |

반영: 1200×800 WebP, 한 장 90 KB 이하. `figure.gscene[data-img=sc_period{n}]`의 안쪽을 `<img>`로 바꾸고 `figcaption`은 그대로 둡니다.

## 4. 캐릭터 팩에서 재사용한 표정 (새로 그릴 것 없음)

| 캐릭터 | 쓴 표정 번호 |
|---|---|
| 박사 `doc` | e09 · e10 · e13 · e16 |
| 조수 하루 `asst` | e01 · e07 · e12 · e13 · e16 · e24 |
| 초파리 연구원 `fly` | e08 · e09 · e13 |
| 주판봇 `robo` | e09 · e13 · e16 |
| 인턴 시아 `sia` | e07 · e09 · e10 · e13 · e15 · e17 |
| 인턴 모아 `moa` | e01 · e04 · e07 · e09 · e12 · e13 · e16 · e19 · e24 |
| 미공개 `x1`·`x2`·`x3` | x1 e13 · x2 e01, e13 · x3 e09, e13, e16 |

주판봇은 기준 표정 9종(E13·E01·E03·E02·E04·E09·E16·E15·E24) 안에서만 골랐습니다. 미공개 식구는 버튼을 눌러야 보이는 자리(식구 명부, 쉬는 시간 암기 카드)에만, 밝은 카드 위에 둡니다.

## 5. 일관성 지침
- 인턴 두 명이 주인공입니다. 장면마다 두 사람을 가운데에 둡니다.
- 박사는 출제자입니다. 교시 장면에서는 뒤에서 지켜보는 자리에만 둡니다.
- 시험 결과(누가 몇 점인지)를 암시하는 그림을 넣지 않습니다.
- 박사·조수·시아·모아는 좌우 반전하지 않습니다(머리 장식·브릿지 위치가 바뀝니다).

## 6. 넘겨받은 뒤 처리
표지 → `cover_manifest.json`의 `cover` 항목 `status`를 `done`으로, `path`에 파일 이름을 적습니다. 교시 장면도 같습니다. 표지를 넣을 때 `twitter:card`를 `summary_large_image`로 바꾸고 `og:image`를 더합니다.

## 7. 체크리스트
- [ ] 그림 안에 글자·숫자·로고 없음
- [ ] 여섯 캐릭터 외형이 참고 그림과 같음 (주판봇: 베이지 상자형, 주판알 안테나, 무한궤도)
- [ ] 흰 둥근 로봇·금화 없음
- [ ] 미공개 X1~X3가 표지·교시 장면에 없음
- [ ] 얼굴과 손이 안전 영역 안
- [ ] 파일 크기: 표지 220 KB, 장면 90 KB 이하 · 페이지 전체 600 KB 이하

## 8. 매니페스트
`cover_manifest.json` (저장소 맨 위 폴더) — 표지 1, 교시 장면 4, 온톨로지 위치(`index.html`의 `#kg`·`#export`), 언어 `ko`.
