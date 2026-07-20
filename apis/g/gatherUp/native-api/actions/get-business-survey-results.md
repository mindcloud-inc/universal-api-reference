# Get Business Survey Results with GatherUp

Retrieves business survey results from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/survey-questions/average/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Get Business Survey Results](https://app.gatherup.com/api/doc/survey-questions/average/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `from` | body | `string` | no | Received from |
| `to` | body | `string` | no | Received to |
