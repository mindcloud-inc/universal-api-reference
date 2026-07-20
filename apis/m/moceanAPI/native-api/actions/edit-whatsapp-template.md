# Edit WhatsApp Template with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/template/whatsapp/:templateId`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Edit WhatsApp Template](https://moceanapi.com/docs#editing-whatsapp-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Updated template category when allowed. |
| `components` | body | `string` | no | Updated JSON array string of template components. |
| `templateId` | path | `string` | yes | The WhatsApp template ID to edit. |
