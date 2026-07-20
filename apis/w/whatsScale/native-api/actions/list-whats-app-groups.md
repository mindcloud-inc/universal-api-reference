# List WhatsApp Groups with WhatsScale

Retrieves WhatsApp groups from a WhatsScale session.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/:session/groups`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [List WhatsApp Groups](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Session name from /api/sessions. |
