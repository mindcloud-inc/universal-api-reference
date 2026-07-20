# Get Record with Castor EDC

Retrieves a record from Castor EDC by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/record/:record_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Get Record](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `record_id` | path | `string` | yes | Record ID of the Record to fetch |
