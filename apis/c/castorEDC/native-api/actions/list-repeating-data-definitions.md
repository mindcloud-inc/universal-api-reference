# List Repeating Data Definitions with Castor EDC

Retrieves repeating data definitions from Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/repeating-data`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Repeating Data Definitions](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
