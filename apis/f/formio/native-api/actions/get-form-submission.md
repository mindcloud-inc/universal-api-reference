# Get Form Submission with Form.io

Retrieves a form submission from your Form.io project.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/:formId/submission/:submissionId`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Get Form Submission](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID containing the submission. |
| `submissionId` | path | `string` | yes | The submission ID. |
