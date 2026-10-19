# greet-ci

인사말 프로그램 및 GitHub Actions CI 실습

## 설치 및 환경 설정

uv를 사용하여 개발 의존성을 동기화합니다.

```bash
uv sync --locked
```

## 실행

```bash
# 이름을 인수로 전달하여 실행
uv run --locked python greet.py Hee
# 출력: Hello, Hee!

# 인수를 생략하고 실행 (기본값: world)
uv run --locked python greet.py
# 출력: Hello, world!
```

## 테스트 및 코드 품질 검사

```bash
# 단위 테스트 실행
uv run --locked pytest -q greet.py

# 코드 포맷 검사
uv run --locked black --check greet.py

# 린트 검사
uv run --locked flake8 greet.py

# 타입 검사
uv run --locked mypy greet.py

# 패키지 빌드
uv build
```
