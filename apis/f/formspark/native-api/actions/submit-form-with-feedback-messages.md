# Submit Form With Feedback Messages with Formspark

Creates a Formspark form submission with custom feedback messages.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Feedback Messages](https://documentation.formspark.io/customization/feedback-page.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `_feedback.success.title` | body | `string` | no | Custom success title for the hosted Formspark feedback page. |
| `_feedback.success.message` | body | `string` | no | Custom success message for the hosted Formspark feedback page. |
| `_feedback.error.title` | body | `string` | no | Custom error title for the hosted Formspark feedback page. |
| `_feedback.error.message` | body | `string` | no | Custom error message for the hosted Formspark feedback page. |
