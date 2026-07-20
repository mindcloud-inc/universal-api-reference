# Create Or Update Template with UniOne

Creates or updates an email template in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `template/set.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Create Or Update Template](https://docs.unione.io/en/web-api-ref#template-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template.id` | body | `string` | no | Template identifier. Reuse the same value to update an existing template. |
| `template.name` | body | `string` | yes | Template display name. |
| `template.editor_type` | body | `string` | yes | Template editor type. |
| `template.template_engine` | body | `string` | yes | Template engine used for substitutions. |
| `template.body.html` | body | `string` | yes | HTML content of the template body. |
| `template.body.plaintext` | body | `string` | no | Plaintext fallback content for the template body. |
| `template.subject` | body | `string` | yes | Template subject line. |
| `template.from_email` | body | `string` | yes | Sender email stored on the template. |
| `template.from_name` | body | `string` | yes | Sender name stored on the template. |
