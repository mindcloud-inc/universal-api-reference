# Update Organization Member with Whattime

## Endpoint

- **Method:** `PUT`
- **Path:** `/organization_members/:code`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Update Organization Member](https://developer.whattime.co.kr/swagger#/Organization/organizationMemberUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Resource Code |
| `role` | body | `string` | no | 권한   * `owner` : 최고 관리자   * `admin` : 관리자   * `user` : 사용자 |
