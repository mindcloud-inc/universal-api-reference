# List Availabilities with Whattime

## Endpoint

- **Method:** `GET`
- **Path:** `/availabilities`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [List Availabilities](https://developer.whattime.co.kr/swagger#/Availability/availabilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `per` | query | `number` | no | 가져올 개수 |
| `page_token` | query | `string` | no | 가져올 다음페이지 토큰 |
