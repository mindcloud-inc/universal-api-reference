# List Respondent Attributes with Survicate

Retrieves attributes for a specific Survicate respondent.

## Endpoint

- **Method:** `GET`
- **Path:** `/respondents/:respondent_uuid/attributes`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [List Respondent Attributes](https://developers.survicate.com/data-export/respondent/#list-respondents-attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `respondent_uuid` | path | `string` | yes | The unique UUID of the respondent. |
| `start` | query | `string` | no | The attribute identifier used for paginated results. |
