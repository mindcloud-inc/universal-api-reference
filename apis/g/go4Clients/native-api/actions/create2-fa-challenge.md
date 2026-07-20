# Create 2FA Challenge with Go4Clients

Creates a two-factor authentication challenge in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tfa/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create 2FA Challenge](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application` | body | `string` | yes | Application creating the 2FA challenge. |
| `key` | body | `string` | yes | Challenge key, typically a phone number. |
| `validMinutes` | body | `number` | no | Expiration time in minutes for the generated code. |
| `maxAttempts` | body | `number` | no | Maximum validation attempts before the code is blocked. |
