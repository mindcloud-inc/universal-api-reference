# Send Transactional Email with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/email/send`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Send Transactional Email](https://platform.hyax.com/api-docs/email-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient email address. |
| `subject` | body | `string` | yes | Email subject. |
| `html` | body | `string` | no | HTML email body. Provide HTML or text. |
| `text` | body | `string` | no | Plain text email body. Provide text or HTML. |
