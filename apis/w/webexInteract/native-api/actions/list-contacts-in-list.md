# List contacts in list with Webex Interact

Retrieves contacts from a list in Webex Interact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/v1/contacts/list/{listId}`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [List contacts in list](https://docs.webexinteract.com/reference/contacts-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated contact fields to return. |
| `listId` | path | `string` | yes | Contact list ID whose contacts should be returned. |
| `search` | query | `string` | no | Exact phone or WhatsApp number search. |
