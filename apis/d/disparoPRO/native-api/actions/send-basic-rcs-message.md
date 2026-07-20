# Send Basic RCS Message with Disparo PRO

Creates a basic RCS message in Disparo PRO.

## Endpoint

- **Method:** `POST`
- **Path:** `/message/basic`
- **Base URL:** `https://gateway.disparopro.com.br/rcs`
- **Official documentation:** [Send Basic RCS Message](https://painel.disparopro.com.br/docs/rcs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Basic text message body. |
| `template_id` | body | `string` | no | Registered template ID. |
| `variables` | body | `object` | no | Variables mapping for the selected template. |
| `to` | body | `string` | yes | Recipient phone number in E.164 format. |
| `partner_data` | body | `object` | no | Additional integration data returned in webhooks. |
