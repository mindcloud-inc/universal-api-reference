# Create Calendar Connection with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/connects`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Create Calendar Connection](https://developer.whattime.co.kr/swagger#/Connect/connectsCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `string` | no | User uri |
| `kind` | body | `string` | yes | — |
| `email` | body | `string` | yes | 아이디(이메일) |
| `password` | body | `string` | yes | 비밀번호 |
