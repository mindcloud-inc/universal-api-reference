# List Calendars with Whattime

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [List Calendars](https://developer.whattime.co.kr/swagger#/Calendar/calendars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | no | Organization uri (User 모델에 organization.uri 를 참고해 주세요) |
| `user` | query | `string` | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `active` | query | `boolean` | no | 활성화 여부 |
| `sort` | query | `string` | no | 정렬 필드 `id` : 생성일, `name` : 이름 |
| `order` | query | `string` | no | 오름,내림 차순 |
| `per` | query | `number` | no | 가져올 개수 |
| `page_token` | query | `string` | no | 가져올 다음페이지 토큰 |
