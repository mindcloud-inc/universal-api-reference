# Get Alert Details with SIGNL4

Retrieves alert details from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/alerts/{alertId}/details`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Alert Details](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Alert you want to get. |
| `userId` | query | `string` | no | User ID of user in which behave the api is called. It is used for filtering purposes regarding the alert. |
