# 사용자 정보 조회 API

## 개요
이 API는 시스템에 등록된 특정 사용자의 상세 정보를 조회하기 위한 엔드포인트입니다. 사용자의 ID를 기반으로 정보를 검색하고, 사용자의 이름, 이메일 등의 기본 정보를 반환합니다.

## 에러 코드 및 메시지
| 에러 코드 | 메시지                   | 설명                                    |
|-----------|--------------------------|-----------------------------------------|
| 400       | Bad Request              | 잘못된 요청 구조입니다.                   |
| 401       | Unauthorized             | 인증 정보가 유효하지 않습니다.              |
| 404       | Not Found                | 요청한 사용자를 찾을 수 없습니다.           |
| 500       | Internal Server Error    | 서버 내부 에러가 발생했습니다.             |

## API 엔드포인트

### 엔드포인트: 사용자 정보 조회
- **URL**: `/api/users/{userId}`
- **Method**: GET
- **URL Params**:
    - `userId=[integer]`: 조회하고자 하는 사용자의 ID
- **Success Response**:
    - **Code**: 200
    - **Content**:

### 정상 처리 시 응답 값
```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john.doe@example.com",
  "created_at": "2021-01-01T00:00:00Z"
}
```

### 에러 처리 시 응답 값
```json
{
  "error": {
    "code": 404,
    "message": "User not found",
    "details": "The user with the specified ID does not exist."
  }
}
```

### Dev 환경 호출 예시
```http request
http://apid.example.com/api/users/123
```