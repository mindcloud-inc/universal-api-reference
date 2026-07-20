# Get Submission with 123FormBuild

Retrieves a submission from a form in 123FormBuilder.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/{form_id}/submissions/{submission_id}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Get Submission](https://www.123formbuilder.com/developer/api-v2-forms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form |
| `submission_id` | path | `number` | yes | The ID of the submission |
| `include_recipients` | query | `string` | no | Return the recipient(s) who should receive the submission |
