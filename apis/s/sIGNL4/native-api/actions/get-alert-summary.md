# Get Alert Summary with SIGNL4

Retrieves an alert summary from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/alerts/{alertId}/summary`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Alert Summary](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alertId` | path | `string` | yes | Id of the alert to get the summary for |
| `language` | query | `string` | no | Language of the requested summary |
