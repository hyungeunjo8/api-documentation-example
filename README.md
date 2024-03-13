# API 문서 작성 가이드

**API 버전 명시**

- API의 변경이 발생할 때마다 기존 클라이언트와의 호환성을 유지하기 위해 API 버전을 명확히 지정합니다. 버전 정보는 URI에 포함시킬 수 있으며, 예를 들어 `/api/v1/users`와 같이 표현할 수 있습니다.

**HTTP Method**

- `GET`: 리소스 조회
- `POST`: 리소스 생성
- `PUT`: 리소스 수정
- `PATCH`: 리소스 부분 수정

**HTTP 상태 코드**

- `200 OK`: 요청 성공
- `201 Created`: 새 리소스 생성 성공
- `400 Bad Request`: 잘못된 요청
- `401 Unauthorized`: 인증 실패
- `404 Not Found`: 리소스를 찾을 수 없음
- `500 Internal Server Error`: 서버 에러 발생 시

요청/응답 표현 방식: …

페이징 처리 API 제공 시: …

에러 응답 시: …

기타…