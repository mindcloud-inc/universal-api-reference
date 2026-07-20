# List Facebook Recommendations with GatherUp

Retrieves Facebook recommendations received in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/facebook-recommendations/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Facebook Recommendations](https://app.gatherup.com/api/doc/facebook-recommendations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | no | Business id (or multiple comma-separated ids.) |
| `from` | body | `string` | no | Received from |
| `to` | body | `string` | no | Received to |
| `page` | body | `number` | no | Page |
