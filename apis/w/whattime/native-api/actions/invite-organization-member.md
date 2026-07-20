# Invite Organization Member with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/organization_members`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Invite Organization Member](https://developer.whattime.co.kr/swagger#/Organization/organizationMemberCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | 이메일 |
| `role` | body | `string` | no | 권한   * `owner` : 최고 관리자   * `admin` : 관리자   * `user` : 사용자 |
