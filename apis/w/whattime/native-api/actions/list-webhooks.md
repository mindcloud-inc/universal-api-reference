# List Webhooks with Whattime

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [List Webhooks](https://developer.whattime.co.kr/swagger#/Webhook/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | no | Organization uri (User 모델에 organization.uri 를 참고해 주세요) |
| `user` | query | `string` | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `kind` | query | `string` | no | 콜벡 종류 |
| `per` | query | `number` | no | 가져올 개수 |
| `page_token` | query | `string` | no | 가져올 다음페이지 토큰 |
