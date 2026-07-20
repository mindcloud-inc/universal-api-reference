# Download WhatsApp Rich Media with Mocean API

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/2/media/whatsapp`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Download WhatsApp Rich Media](https://moceanapi.com/docs#download-rich-media)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-from` | query | `string` | yes | Registered WhatsApp Business sender phone number. |
| `mocean-media-id` | query | `string` | yes | The Mocean media ID to download. |
