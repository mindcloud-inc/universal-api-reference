# Get Form with Castor EDC

Retrieves a form from Castor EDC by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/form/:form_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Get Form](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `form_id` | path | `string` | yes | The form UUID. |
