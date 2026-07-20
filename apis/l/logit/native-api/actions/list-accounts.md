# List Accounts with Logit

Retrieves accounts from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/accounts`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [List Accounts](https://logit.io/docs/developer-api/account-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Enabled` | query | `boolean` | no | Filter accounts by enabled status. |
| `Paying` | query | `boolean` | no | Filter accounts by paying status. |
