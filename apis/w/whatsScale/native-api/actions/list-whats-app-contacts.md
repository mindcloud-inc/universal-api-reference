# List WhatsApp Contacts with WhatsScale

Retrieves WhatsApp contacts from a WhatsScale session.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/:session/contacts`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [List WhatsApp Contacts](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Session name from /api/sessions. |
