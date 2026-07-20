# Update User with Whattime

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:code`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Update User](https://developer.whattime.co.kr/swagger#/User/usersUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Resource Code |
| `name` | body | `string` | no | 이름 |
