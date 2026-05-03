# API Spec Guide

## 목적

API 명세를 일관되게 관리하기 위한 작성 가이드입니다.

## endpoint 템플릿

```text
[METHOD] /api/example
```

## 작성 예시

### [POST] /api/users

설명: 사용자 생성

Request:

```json
{
  "email": "user@example.com",
  "password": "string"
}
```

Response:

```json
{
  "id": 1,
  "email": "user@example.com"
}
```

Error:

```json
{
  "code": "INVALID_INPUT",
  "message": "email is invalid"
}
```

## 작성 원칙

- 요청/응답 예시는 실제 필드명 기준으로 작성합니다.
- 에러 응답 형식을 통일합니다.
- 인증 필요 여부를 명시합니다.
- 상태 코드와 예외 케이스를 함께 적습니다.

## 추가 권장 사항

- Swagger/OpenAPI를 사용한다면 문서 위치를 README에 연결합니다.
- API 변경 시 PR에 명세 변경 여부를 체크합니다.
