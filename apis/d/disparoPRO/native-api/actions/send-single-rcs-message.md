# Send Single RCS Message with Disparo PRO

Creates a single RCS message in Disparo PRO.

## Endpoint

- **Method:** `POST`
- **Path:** `/message/single`
- **Base URL:** `https://gateway.disparopro.com.br/rcs`
- **Official documentation:** [Send Single RCS Message](https://painel.disparopro.com.br/docs/rcs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Registered template ID. |
| `variables` | body | `object` | yes | Variables mapping for the selected template. |
| `to` | body | `string` | yes | Recipient phone number in E.164 format. |
| `partner_data` | body | `object` | no | Additional integration data returned in webhooks. |
