# List Reservations with Whattime

## Endpoint

- **Method:** `GET`
- **Path:** `/reservations`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [List Reservations](https://developer.whattime.co.kr/swagger#/Reservation/reservations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | no | Organization uri (User 모델에 organization.uri 를 참고해 주세요) |
| `user` | query | `string` | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `status` | query | `string` | no | 상태 |
| `email` | query | `string` | no | 이메일 |
| `name` | query | `string` | no | 이름 |
| `min_start_at` | query | `string` | no | 시간 검색 시작시간 |
| `max_start_at` | query | `string` | no | 시간 검색 종료시간 |
| `sort` | query | `string` | no | 정렬 필드 `id` : 생성일, `start_at` : 시작시간 |
| `order` | query | `string` | no | 오름,내림 차순 |
| `per` | query | `number` | no | 가져올 개수 |
| `page_token` | query | `string` | no | 가져올 다음페이지 토큰 |
