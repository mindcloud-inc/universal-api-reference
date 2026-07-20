# Get Authenticated User with Yandex ID

## Endpoint

- **Method:** `GET`
- **Path:** `/info`
- **Base URL:** `https://login.yandex.ru`
- **Official documentation:** [Get Authenticated User](https://yandex.com/dev/id/doc/en/user-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jwt_secret` | query | `string` | no | Optional shared secret for validating OpenID JWT responses when you request JWT format from Yandex. |
