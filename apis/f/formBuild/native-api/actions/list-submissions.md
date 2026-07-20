# List Submissions with 123FormBuild

Retrieves submissions from a form in 123FormBuilder.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/{form_id}/submissions`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [List Submissions](https://www.123formbuilder.com/developer/api-v2-forms/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form |
| `start_date` | query | `date` | no | List submissions starting with a specific date |
| `start_submission_id` | query | `number` | no | List submissions starting with the specified submission ID |
| `include_recipients` | query | `string` | no | Return the recipient(s) who should receive the submissions |
