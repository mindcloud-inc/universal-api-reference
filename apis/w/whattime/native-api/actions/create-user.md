# Create User with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Create User](https://developer.whattime.co.kr/swagger#/User/usersCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | 이메일 |
| `name` | body | `string` | yes | 이름 |
| `password` | body | `string` | yes | 패스워드 |
| `role` | body | `string` | no | 권한   * `owner` : 최고 관리자   * `admin` : 관리자   * `user` : 사용자 |
| `time_zone` | body | `string` | no | 타임존 |
