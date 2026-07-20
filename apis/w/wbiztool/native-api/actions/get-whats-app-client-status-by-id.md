# Get WhatsApp Client Status By Id with Wbiztool

Retrieves a specific WhatsApp client status by ID from Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/status/{{whatsapp_client_id}}/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Get WhatsApp Client Status By Id](https://wbiztool.com/docs/whatsapp-client-status-by-id-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsapp_client_id` | path | `number` | yes | WhatsApp client ID to check in the URL path. |
