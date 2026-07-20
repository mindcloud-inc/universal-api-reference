# List Account Stacks with Logit

Retrieves stacks for an account from Logit.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account/:accountId/stacks`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [List Account Stacks](https://logit.io/docs/developer-api/account-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | The ID of a Logit account. |
