# List Queries with Castor EDC

Retrieves study queries from Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/query`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Queries](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `page` | query | `number` | no | The page to retrieve |
