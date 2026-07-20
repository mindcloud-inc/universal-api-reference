# Validate 2FA Challenge with Go4Clients

Validates a Go4Clients two-factor authentication code.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tfa/v1.0/validate`
- **Base URL:** `https://cloud.go4clients.com:8580`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application` | body | `string` | yes | Application that created the two-factor authentication challenge. |
| `key` | body | `string` | yes | Telephone number or key associated with the challenge. |
| `code` | body | `string` | yes | Code to validate. |
