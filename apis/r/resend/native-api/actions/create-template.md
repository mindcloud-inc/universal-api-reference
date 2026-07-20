# Create Template with Resend

Creates a new template in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Create Template](https://resend.com/docs/api-reference/templates/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Template name. |
| `html` | body | `string` | yes | HTML content for the template. |
| `alias` | body | `string` | no | Optional template alias. |
| `from` | body | `string` | no | Sender email address. |
| `subject` | body | `string` | no | Template subject line. |
| `text` | body | `string` | no | Plain-text content for the template. |
