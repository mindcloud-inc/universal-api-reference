# Search Contacts with 2Chat

Finds contacts in 2Chat by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/search`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Search Contacts](https://developers.2chat.co/docs/API/Contacts/search-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search text matched against contact fields. |
| `channel_uuid` | query | `string` | no | Limit results to a specific WhatsApp channel UUID. |
