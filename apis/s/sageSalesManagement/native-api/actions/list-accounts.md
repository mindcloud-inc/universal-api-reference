# List Accounts with Sage Sales Management

Retrieves accounts from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [List Accounts](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based page number to return. |
| `where` | query | `string` | no | SQL-like filter expression supported by Sage Sales Management. |
| `order` | query | `string` | no | Field name used to sort the result set. |
