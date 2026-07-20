# List Show-Hide History with GatherUp

Retrieves show-hide history records from GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedbacks/show-hide-history`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Show-Hide History](https://app.gatherup.com/api/doc/feedbacks/show-hide-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | no | Business id (or multiple comma-separated ids.) |
| `from` | body | `string` | no | Received from |
| `page` | body | `number` | no | Page |
| `to` | body | `string` | no | Received to |
