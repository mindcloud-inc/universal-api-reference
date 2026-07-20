# Export Study Data with Castor EDC

Exports study data from Castor EDC as a dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/export/data`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Export Study Data](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `exclude_empty_surveys` | query | `boolean` | no | Exclude survey instances without data points |
| `exclude_empty_reports` | query | `boolean` | no | Exclude report instances without data points |
| `archived` | query | `boolean` | no | Include archived data |
