# List Records with Castor EDC

Retrieves study records from Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/record`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Records](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `institute` | query | `string` | no | Institute UUID to filter on |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `page` | query | `number` | no | The page to retrieve |
| `archived` | query | `number` | no | Filter archived records using 0 or 1 |
