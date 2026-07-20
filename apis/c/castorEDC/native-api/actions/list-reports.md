# List Reports with Castor EDC

Retrieves reports from a study in Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/report`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Reports](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
