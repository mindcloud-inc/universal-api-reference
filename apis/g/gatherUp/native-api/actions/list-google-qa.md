# List Google Q&A with GatherUp

Retrieves Google Q&A entries from GatherUp.

## Endpoint

- **Method:** `GET`
- **Path:** `/google-qa/get`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [List Google Q&A](https://app.gatherup.com/api/doc/google-qa/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | query | `number` | no | Business id. |
| `search` | query | `string` | no | The string which you are looking for. |
| `locations` | query | `string` | no | Business IDs separated by a comma. |
| `status` | query | `string` | no | Status questions separated by a comma. |
| `labels` | query | `string` | no | User labels separated by a comma. |
| `page` | query | `number` | no | Page number |
