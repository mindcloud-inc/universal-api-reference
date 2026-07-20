# Get Field with Castor EDC

Retrieves a field from Castor EDC by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/field/:field_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Get Field](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `field_id` | path | `string` | yes | The field UUID. |
| `include` | query | `string` | no | Comma-separated list of extra field properties to include. Send multiple values as a string separated by `,`. |
