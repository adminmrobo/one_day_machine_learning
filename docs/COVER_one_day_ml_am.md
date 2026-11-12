# 표지 지시문 — 「하루에 다 끝내는 머신러닝 서머리 노트 · 오전반」

## 선정 (2026-11-13)

표지는 **하품하는 표정의 시아와 모아**로 정했습니다. 기준 그림은 「05_Yawning」(밝은 낮의 사무실에서 하품하는 시아)입니다.

| 항목 | 내용 |
|---|---|
| 키 · 판 | cover_one_day_ml_am · L (16:9, 1920 이상) |
| 그림체 | 기준 그림과 같은 부드러운 애니메이션 일러스트 (픽셀아트 아님) |
| 장소 (앵커) | 밝은 낮의 고층 사무실. 큰 창밖으로 도시가 보임 (생활·현장 앵커) |
| 주제 은유 | 책상 위에 쌓인 서류와 공책, 모니터 두 대, 컵 — 시험 전날 벼락치기의 피로 |
| 캐릭터 포즈 | 시아: 의자에 앉아 한 손으로 입을 가리고 크게 하품 (기준 그림 그대로) / 모아: 시아 옆자리에서 같은 표정으로 하품. 한 손은 입을 가리고 다른 손에는 형광펜 |
| 대체 글 (alt) | 밝은 낮의 사무실. 창밖으로 도시가 보이는 책상에서 인턴 시아와 모아가 나란히 앉아 한 손으로 입을 가리고 크게 하품합니다. 책상에는 모니터와 서류 더미, 컵이 놓여 있습니다 |
| 등장 | 시아와 모아 두 명만. 다른 식구는 표지에 넣지 않음 |

## 지금 상태

- `cover_one_day_ml_am.webp` (1600×893, 97 KB): 기준 그림 그대로 넣었습니다. **시아만 있습니다.**
- `og_one_day_ml_am.jpg` (1200×630): 같은 그림에 제목을 얹어 만들었습니다.
- `thumb_one_day_ml_am.webp` (600×400): 같은 그림에서 시아 쪽을 잘랐습니다.
- 모아가 함께 있는 그림을 받으면 세 파일을 모두 바꿉니다.

## 시아 + 모아 그림 요청 (Genspark에 붙여 넣기 ↓)

**참고 이미지 (함께 올리기):** ① 기준 그림 「05_Yawning」 ② 모아 기본 그림 (`adminmrobo/fruitfly-lab-expressions`의 `images/moa/E13_neutral.png`, 졸린 표정 `E17_sleepy.png`)

```
첨부한 첫 번째 그림(하품하는 흑발 메이드)과 같은 그림체·같은 장소·같은 구도로, 두 번째 인물을 더한 표지 그림 1장을 만들어 줘.
- 비율 16:9, 가로 1920px 이상
- 첫 번째 그림의 인물(시아)은 외형·표정·자세를 그대로 유지
- 그 옆자리에 두 번째 참고 그림의 인물(모아)을 같은 표정(크게 하품)으로 추가
- 그림 안에 글자·숫자·로고를 넣지 말 것 (모니터와 서류는 뜻 없는 선이나 빈 화면으로)
- 두 사람의 얼굴과 손은 가장자리에서 떨어진 가운데 영역에
- 아래 영어 프롬프트를 그대로 써 줘

Wide 16:9 illustration in exactly the same soft anime illustration style, lighting and colour palette as the first attached image: a bright daytime high-rise office with large windows and a hazy city skyline, pale warm light.
Keep the first character exactly as she is: a calm young woman with long straight jet-black hair and side-swept bangs, gray eyes, small drop earrings, charcoal-black maid dress with a large gray bow and a long white frilled apron, sitting on an office chair, covering a big yawn with her right hand, eyes half closed and slightly teary.
Add a second character sitting at the desk right next to her, drawn in the same style: a gentle young woman with long ash-beige wavy hair, a white frilled maid headband with a ribbon over her left ear, amber eyes, a camel knit cardigan over a white blouse and a white frilled apron. She is yawning in the same way, one hand covering her mouth, eyes half closed and slightly teary, her other hand loosely holding a highlighter pen over an open notebook.
Desk: two monitors with blank dark screens, a stack of blank papers, an open notebook, one pink takeaway cup. No readable text anywhere.
Composition: both characters in the central area (12% margin left and right, 10% top, 18% bottom); the black-haired character on the left, the beige-haired character on the right; keep the upper-right area simple and bright.
Mood: sleepy but warm, two interns worn out from cramming the day before a quiz.
No text, no letters, no numbers, no logos, no real brands, no cigarettes, no alcohol.
```

**고칠 때 (같은 대화에서):** `Same characters, same art style and composition. Change only: {고칠 점}. Still no text.`

## 점검

- 두 사람 모두 하품하는 표정인가 (한 손으로 입을 가림)
- 시아: 흑발 긴 생머리, 머리 장식 없음, 회색 눈, 회색 큰 리본 / 모아: 애쉬 베이지 웨이브, 왼쪽 귀 위 리본 달린 헤드밴드, 호박색 눈, 카멜 가디건
- 좌우 반전 금지 (모아의 리본은 왼쪽 귀 위)
- 그림 안에 읽히는 글자가 없는가 — 기준 그림에는 서류와 모니터에 글자 비슷한 무늬가 있습니다. 새 그림에서는 비워 달라고 요청했습니다
- 바탕이 밝은가 (페이지가 흰 모눈 바탕입니다)

## 반영

1600×900 안팎 WebP 220 KB 이하로 줄여 `cover_one_day_ml_am.webp`를 바꿔 넣습니다. `index.html`은 그대로 두고 `alt`만 위 대체 글로 고칩니다. 공유 미리보기와 썸네일은 새 그림에서 다시 만듭니다.
