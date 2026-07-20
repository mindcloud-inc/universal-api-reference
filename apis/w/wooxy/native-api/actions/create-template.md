# Create Template with Wooxy

Creates a new template in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/template/email/create`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Template](https://wooxy.com/api-documentation/templates/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The template name. |
| `subject` | body | `string` | yes | The email subject. |
| `html` | body | `string` | yes | The full HTML or text content of the template. |
