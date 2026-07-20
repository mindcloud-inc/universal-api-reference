# List Forms with Castor EDC

Retrieves forms from a study in Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/form`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Forms](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
