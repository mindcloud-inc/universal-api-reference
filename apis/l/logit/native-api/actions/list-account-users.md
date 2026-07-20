# List Account Users with Logit

Retrieves users for an account from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account/:accountId/users`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [List Account Users](https://logit.io/docs/developer-api/account-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The ID of a Logit account. |
