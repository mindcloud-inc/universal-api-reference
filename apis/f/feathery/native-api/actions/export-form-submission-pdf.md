# Export Form Submission PDF with Feathery

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/submission/pdf/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Export Form Submission PDF](https://api-docs.feathery.io/#export-form-submission-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | body | `string` | yes | The unique ID of the form whose submission you want to export. |
| `user_id` | body | `string` | yes | The unique ID corresponding to the Feathery submission or user you want to export. |
