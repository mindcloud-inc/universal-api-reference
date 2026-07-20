# List Contacts with 2Chat

Retrieves contact records from 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [List Contacts](https://developers.2chat.co/docs/API/Contacts/list-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_uuid` | query | `string` | no | Limit results to a specific WhatsApp channel UUID. |
