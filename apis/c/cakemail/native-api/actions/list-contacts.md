# List Contacts with Cakemail

Retrieves contacts from a Cakemail list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/contacts`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [List Contacts](https://cakemail.dev/en/api/contact#show-contacts-of-a-list)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
