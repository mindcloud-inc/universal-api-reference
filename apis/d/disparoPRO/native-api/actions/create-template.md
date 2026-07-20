# Create Template with Disparo PRO

Creates a new template in Disparo PRO.

## Endpoint

- **Method:** `POST`
- **Path:** `/template`
- **Base URL:** `https://gateway.disparopro.com.br/rcs`
- **Official documentation:** [Create Template](https://painel.disparopro.com.br/docs/rcs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | yes | Language code for the template. |
| `category` | body | `string` | yes | Category of the RCS template. |
| `name` | body | `string` | yes | Unique template name. |
| `variables[]` | body | `array<string>` | no | Template variables for dynamic content substitution. |
| `content_type` | body | `object` | yes | Template content configuration. |
| `previous_template_id` | body | `string` | no | Previous template version ID. |
