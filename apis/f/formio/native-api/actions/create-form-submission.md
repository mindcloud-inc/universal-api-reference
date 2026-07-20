# Create Form Submission with Form.io

Creates a new form submission in your Form.io project.

## Endpoint

- **Method:** `POST`
- **Path:** `/form/:formId/submission`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Create Form Submission](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Submission data object keyed by component API keys. |
| `formId` | path | `string` | yes | The form ID that will receive the submission. |
