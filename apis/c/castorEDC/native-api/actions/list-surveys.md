# List Surveys with Castor EDC

Retrieves surveys from a study in Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/survey`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Surveys](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
| `include` | query | `string` | no | Set to forms to include survey forms. |
