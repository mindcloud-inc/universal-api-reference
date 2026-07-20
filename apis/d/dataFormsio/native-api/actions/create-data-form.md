# Create Data Form with DataForms.io

Creates a new data form in DataForms.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/dataforms`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [Create Data Form](https://dataforms.readme.io/reference/update-data-form-copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Template used to create the form. |
| `headline` | body | `string` | yes | The form headline. |
| `type` | body | `string` | yes | The form type. Accepted values: `0`, `1`. |
| `allow_multiple_submissions` | body | `boolean` | no | Allow a user to submit the form multiple times. |
| `lock_after_submission` | body | `boolean` | no | Lock the form after a submission is completed. |
| `redirect_url` | body | `string` | no | Redirect URL to use after form submission. |
