# Get Reporting with Refiner

Retrieves survey reporting data from Refiner.

## Endpoint

- **Method:** `GET`
- **Path:** `/reporting`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Get Reporting](https://refiner.io/docs/api/#get-reporting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | The reporting type: nps, csat, ratings, distribution, or count. |
| `question_identifiers[]` | query | `array<string>` | no | Only include matching question identifiers in the report. |
| `tag_uuids[]` | query | `array<string>` | no | Only include responses tagged with these tag UUIDs. |
| `form_uuids[]` | query | `array<string>` | no | Only include the selected form UUIDs. |
| `segment_uuids[]` | query | `array<string>` | no | Only include the selected segment UUIDs. |
| `date_range_start` | query | `date` | no | Only count data points recorded after this time. |
| `date_range_end` | query | `date` | no | Only count data points recorded before this time. |
