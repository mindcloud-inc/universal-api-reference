# Get Response with Survicate

Retrieves a specific survey response from Survicate.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/:survey_id/responses/:response_uuid`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [Get Response](https://developers.survicate.com/data-export/response/#retrieve-a-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `string` | yes | The unique identifier of the survey containing the response. |
| `response_uuid` | path | `string` | yes | The unique UUID of the response to retrieve. |
