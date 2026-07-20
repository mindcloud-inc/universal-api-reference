# Export Submissions with AbcSubmit

Creates a submission export request for an AbcSubmit form.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/submissions/:form_id/export/:format`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Export Submissions](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form whose submissions you want to export. |
| `format` | path | `string` | yes | The export format: json, xls, or csv. |
