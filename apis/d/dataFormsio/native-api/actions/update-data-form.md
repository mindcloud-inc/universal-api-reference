# Update Data Form with DataForms.io

Updates an existing data form in DataForms.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dataforms/{form_id}`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [Update Data Form](https://dataforms.readme.io/reference/show-data-form-copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The DataForms.io form identifier. |
| `headline` | body | `string` | no | The form headline. |
| `allow_multiple_submissions` | body | `boolean` | no | Allow a user to submit the form multiple times. |
| `lock_after_submission` | body | `boolean` | no | Lock the form after a submission is completed. |
| `redirect_url` | body | `string` | no | Redirect URL to use after form submission. |
