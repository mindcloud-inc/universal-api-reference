# Submit Form With Mail Reply Alias with Formspark

Creates a Formspark form submission using the mail reply alias.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Mail Reply Alias](https://documentation.formspark.io/customization/direct-replies.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `mail` | body | `string` | yes | Email address used as the direct-reply target. |
| `message` | body | `string` | no | Submitted message body. |
