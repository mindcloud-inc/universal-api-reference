# Submit Form With Direct Reply with Formspark

Creates a Formspark form submission with direct reply settings.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Direct Reply](https://documentation.formspark.io/customization/direct-replies.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `_replyto` | body | `string` | no | Email address Formspark should use for direct replies from notification emails. |
