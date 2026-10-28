# 블로그 운영 폴더

매일 1개의 글을 기획·제작·발행하기 위한 작업 공간입니다.

## 역할 분담

| 단계 | 담당 | 결과물 |
|---|---|---|
| 주제 후보 발굴 | Claude | `candidates/YYYY-MM-DD.md` |
| 주제·관점·스타일 결정 | 운영자 | 후보 번호와 요청 사항 전달 |
| 조사·사실 확인·집필·이미지·SEO | Claude | `posts/YYYY-MM-DD/` |
| 편집기 입력·임시저장 | Aside | 플랫폼 임시저장 글 |
| 최종 확인·발행 | 운영자 | 발행 URL |
| 기록·주간 회고 | Claude | `log/publish-log.md` |

## 폴더 구조

```
blog/
├── config/
│   ├── settings.md        # 기본 설정
│   └── style-guide.md     # 문체 가이드 (참고 글 분석 후 작성)
├── candidates/            # 날짜별 주제 후보
├── posts/
│   └── YYYY-MM-DD/
│       ├── post-naver.html
│       ├── post-google.html
│       ├── images/
│       ├── meta.json
│       └── aside-task.md
├── log/
│   └── publish-log.md     # 발행 기록 (일일 한도 확인용)
└── templates/             # 원고·메타·Aside 지시문 템플릿
```

## 하루 흐름

1. Claude가 후보를 `candidates/`에 올리고 알린다.
2. 운영자가 후보를 고른다. 선택 전에는 본문 작성이나 이미지 생성을 하지 않는다.
3. Claude가 `posts/YYYY-MM-DD/`에 완성본을 올린다.
4. 운영자가 `aside-task.md` 내용을 Aside에 붙여넣는다. Aside는 **임시저장까지만** 한다.
5. 운영자가 확인 후 발행하고, URL을 Claude에게 알린다.
6. Claude가 `log/publish-log.md`에 기록한다.

일일 한도는 한국 시간 발행일 기준이다. 발행 전 `log/publish-log.md`에서 같은 날짜의 기록을 확인한다.
