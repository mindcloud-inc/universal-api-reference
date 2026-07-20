# Create Contacts with ChatDaddy

Creates or updates contacts in ChatDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/upsert`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Create Contacts](https://chatdaddy.stoplight.io/docs/openapi/243d11ecc97e7-create-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Contact payloads to create or upsert. |
