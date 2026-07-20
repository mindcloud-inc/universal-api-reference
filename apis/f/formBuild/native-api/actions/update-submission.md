# Update Submission with 123FormBuild

Updates an existing submission in a 123FormBuilder form.

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/{form_id}/submissions/{submission_id}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Update Submission](https://www.123formbuilder.com/developer/api-v2-forms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form |
| `submission_id` | path | `number` | yes | The ID of the submission |
| `payed` | query | `string` | no | Payment status for the submission |
| `approved` | query | `number` | no | Approval status for the submission |
