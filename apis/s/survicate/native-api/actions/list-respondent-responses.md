# List Respondent Responses with Survicate

Retrieves responses from a specific Survicate respondent.

## Endpoint

- **Method:** `GET`
- **Path:** `/respondents/:respondent_uuid/responses`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [List Respondent Responses](https://developers.survicate.com/data-export/respondent/#list-respondents-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `respondent_uuid` | path | `string` | yes | The unique UUID of the respondent whose responses are being requested. |
| `start` | query | `string` | no | Include responses collected before this ISO 8601 timestamp with microseconds. |
