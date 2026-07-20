# Create Questionnaire Request with Conveyor

Creates a questionnaire request in Conveyor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/questionnaire_requests`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Create Questionnaire Request](https://docs.conveyor.com/reference/post-questionnaire-requests)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | no | External questionnaire request identifier. |
| `source` | body | `string` | no | Source system for the request. |
| `submitter_email` | body | `string` | no | Submitter email address. |
| `submitter_external_id` | body | `string` | no | External submitter identifier. |
| `submitter_external_name` | body | `string` | no | External submitter name. |
| `case_ids` | body | `string<string>` | no | Salesforce case identifiers for questionnaire import. |
| `raw_data` | body | `string` | no | Raw questionnaire request data. |
| `file` | body | `file` | no | Questionnaire request file upload. |
