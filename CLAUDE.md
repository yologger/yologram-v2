# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

yologram-v2는 모노레포 구조의 프로젝트로, 프론트엔드(Next.js)와 백엔드(FastAPI) 두 개의 서브 프로젝트로 구성.

## Repository Structure

- web/ — Next.js 기반 프론트엔드 (패키지명: yologram-v2-web)
- api/ — FastAPI 기반 백엔드 API (패키지명: yologram-v2-api)

## Build & Run

### Web (web/)
```
cd web
npm install
npm run dev        # 개발 서버
npm run build      # 프로덕션 빌드
npm run lint       # 린트
```

### API (api/)
```
cd api
pip install -r requirements.txt
uvicorn main:app --reload   # 개발 서버
```

## CI/CD

- GitHub Actions 기반. api/, web/ 경로별로 별도 워크플로우가 트리거됨.
- 배포 대상: AWS App Runner (고려 중)

## Rules

- 코드 변경 시 반드시 README.md, CLAUDE.md, AGENTS.md를 함께 업데이트할 것.
- 코드 변경 전 항상 plan을 먼저 제시하고, 승인 후 적용할 것.
- 각 서브 프로젝트는 독립적으로 실행. 루트에는 공통 설정 없음.
- 프로젝트 초기 단계이므로 구조가 확정되면 이 문서를 업데이트할 것.
