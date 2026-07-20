# List Fields with Castor EDC

Retrieves fields from a study in Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/field`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Fields](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
| `include` | query | `string` | no | Comma-separated list of extra field properties to include. Send multiple values as a string separated by `,`. |
