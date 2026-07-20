# List Survey Package Instances with Castor EDC

Retrieves survey package instances from Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/survey-package-instance`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Survey Package Instances](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
| `page_size` | query | `number` | no | Page size to retrieve. |
| `participant_id` | query | `string` | no | Filter results by participant UUID. |
| `ccr_patient_id` | query | `string` | no | Filter results by CCR patient identifier. |
| `sort` | query | `string` | no | Sort field. |
| `dir` | query | `string` | no | Sort direction ASC or DESC. |
| `available_from_start` | query | `string` | no | Start of the available_from date range. |
| `available_from_end` | query | `string` | no | End of the available_from date range. |
| `available` | query | `boolean` | no | Filter by whether the survey package instance is currently available. |
| `archived` | query | `boolean` | no | Filter by archived status. |
| `repeatable` | query | `boolean` | no | Filter mobile survey packages generated from repeatable surveys. |
| `training` | query | `boolean` | no | Filter mobile survey packages belonging to training configurations. |
| `status` | query | `string` | no | Filter by survey package instance status. |
| `availability_window_start` | query | `string` | no | Start of the availability window range. |
| `availability_window_end` | query | `string` | no | End of the availability window range. |
| `finished_on` | query | `string` | no | Filter by finished date. |
| `finished_on[gt]` | query | `string` | no | Filter by finished date greater than the provided value. |
| `finished_on[gte]` | query | `string` | no | Filter by finished date greater than or equal to the provided value. |
| `finished_on[lt]` | query | `string` | no | Filter by finished date less than the provided value. |
| `finished_on[lte]` | query | `string` | no | Filter by finished date less than or equal to the provided value. |
