# Get Query with Castor EDC

Retrieves a query from Castor EDC by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/query/:query_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Get Query](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `query_id` | path | `string` | yes | Record ID of the Query to fetch |
