# Get User with Qlik

Retrieves a user from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/users/:userId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get User](https://qlik.dev/apis/rest/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Qlik user ID. |
