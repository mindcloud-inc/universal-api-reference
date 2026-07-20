# Download Export with Castor EDC

Downloads an export file from Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/export/:id/download`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Download Export](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `id` | path | `string` | yes | The ID of the Export to download |
