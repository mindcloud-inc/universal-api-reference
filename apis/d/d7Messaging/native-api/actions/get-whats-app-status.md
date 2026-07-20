# Get WhatsApp Status with D7 Messaging

Retrieves WhatsApp delivery status from D7 Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/v2/report/:request_id`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get WhatsApp Status](https://d7networks.com/docs/whatsapp/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by the WhatsApp send action. |
