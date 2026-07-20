# Submit Form With Feedback Page with Formspark

Creates a Formspark form submission with feedback page settings.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Feedback Page](https://documentation.formspark.io/customization/feedback-page.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `_feedback.whitelabel` | body | `string` | no | Remove Formspark branding from the feedback page when the workspace plan supports it. |
| `_feedback.dark` | body | `string` | no | Toggle dark mode on the hosted Formspark feedback page. |
| `_feedback.language` | body | `string` | no | Language code for the hosted Formspark feedback page. |
