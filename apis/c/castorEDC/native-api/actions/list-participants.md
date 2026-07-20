# List Participants with Castor EDC

Retrieves study participants from Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/participant`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Participants](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | no | Site UUID to filter on |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `page` | query | `number` | no | The page to retrieve |
| `archived` | query | `number` | no | Filter archived participants using 0 or 1 |
