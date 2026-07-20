# Delete Form Submission with Form.io

Deletes an existing form submission from your Form.io project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/form/:formId/submission/:submissionId`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Delete Form Submission](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID containing the submission. |
| `submissionId` | path | `string` | yes | The submission ID. |
