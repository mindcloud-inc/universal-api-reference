# List Account Teams with Logit

Retrieves teams for an account from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account/:accountId/teams`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [List Account Teams](https://logit.io/docs/developer-api/account-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The ID of a Logit account. |
