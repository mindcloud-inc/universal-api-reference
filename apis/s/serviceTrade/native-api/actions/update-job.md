# Update Job with ServiceTrade

Updates an existing job in ServiceTrade.

## Endpoint

- **Method:** `PUT`
- **Path:** `job/:jobId`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Update Job](https://api.servicetrade.com/api/docs#resource-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | Job to update. |
| `description` | body | `string` | no | Updated job description. |
