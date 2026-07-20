# Request Multi Export with Castor EDC

Requests multiple study exports in Castor EDC.

## Endpoint

- **Method:** `POST`
- **Path:** `/study/:study_id/export`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Request Multi Export](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `exports` | body | `object` | yes | Batch export request definition |
