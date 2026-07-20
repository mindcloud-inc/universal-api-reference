# List Organization Members with Whattime

## Endpoint

- **Method:** `GET`
- **Path:** `/organization_members`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [List Organization Members](https://developer.whattime.co.kr/swagger#/Organization/organizationMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `email` | query | `string` | no | 멤버 이메일 |
| `approve` | query | `boolean` | no | 승인 여부 |
| `sort` | query | `string` | no | 정렬 필드 `id` : 생성일, `role` : 권한 , `email` : 이메일 |
| `order` | query | `string` | no | 오름,내림 차순 |
| `per` | query | `number` | no | 가져올 개수 |
| `page_token` | query | `string` | no | 가져올 다음페이지 토큰 |
