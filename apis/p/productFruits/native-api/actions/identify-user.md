# Identify User with Product Fruits

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/identify`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Identify User](https://help.productfruits.com/en/article/rest-api-user-identification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user.firstname` | body | `string` | no | First name of the tracked user. |
| `user.lastname` | body | `string` | no | Last name of the tracked user. |
| `user.role` | body | `string` | no | Role of the tracked user. |
| `user.signUpAt` | body | `date` | no | Signup timestamp in JSON date or datetime format. |
| `user.username` | body | `string` | yes | Unique username of the tracked user. |
