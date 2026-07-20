# Create Account with Sage Sales Management

Creates an account in Sage Sales Management.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Create Account](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Account name |
| `salesRepId1` | body | `number` | yes | Primary sales representative identifier required by ForceManager when creating an account. |
