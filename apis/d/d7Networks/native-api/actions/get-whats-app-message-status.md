# Get WhatsApp Message Status with D7 Networks

Retrieves WhatsApp message status from D7 Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/v2/report/:requestId`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get WhatsApp Message Status](https://d7networks.com/docs/whatsapp/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by a WhatsApp send action. |
