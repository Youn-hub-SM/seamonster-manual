# Seamonster UI/UX Design Manual

씨몬스터 공식몰 디자인 시스템 매뉴얼입니다.
Claude Code와 연동하여 일관된 UI/UX를 구현합니다.

## 사용법

### 1. 저장소 클론
```bash
git clone https://github.com/Youn-hub-SM/seamonster-manual.git
cd seamonster-manual
```

### 2. Claude Code 실행
```bash
claude
```
- `CLAUDE.md`가 자동으로 로드되어 디자인 시스템이 적용됩니다.
- `.claude/settings.json`의 훅이 작업 시 자동으로 `git pull`을 실행합니다.

### 3. 작업 시작
Claude Code에서 평소처럼 작업하면 디자인 시스템이 자동 적용됩니다.

## 파일 구조
```
seamonster-manual/
├── CLAUDE.md                  ← Claude Code 자동 로드 (핵심 규칙)
├── .claude/
│   └── settings.json          ← 자동 pull 훅 설정
├── docs/
│   ├── design-system.md       ← 전체 디자인 시스템 매뉴얼
│   └── claude-prompt.md       ← Claude 프로젝트용 프롬프트
└── README.md
```

## 디자인 시스템 수정
`CLAUDE.md` 또는 `docs/` 파일을 수정하고 push하면 모든 팀원에게 자동 반영됩니다.
