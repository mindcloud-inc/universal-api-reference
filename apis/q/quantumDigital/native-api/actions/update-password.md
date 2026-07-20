# Update Password with Quantum Digital

## Endpoint

- **Method:** `PUT`
- **Path:** `/devplatform/accounts/:dashboardAccountId/password`
- **Base URL:** `https://api.quantumdigital.com`
- **Official documentation:** [Update Password](https://developer.quantumdigital.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currentPassword` | body | `string` | yes | Sensitive value. |
| `newPassword` | body | `string` | yes | Sensitive value. |
| `passwordHint` | body | `string` | no | — |
