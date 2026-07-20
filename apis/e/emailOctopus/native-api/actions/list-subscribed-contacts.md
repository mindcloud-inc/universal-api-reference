# List Subscribed Contacts with EmailOctopus

Retrieves subscribed contacts from an EmailOctopus list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/contacts/subscribed`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [List Subscribed Contacts](https://emailoctopus.com/api-documentation/lists/get-subscribed-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The unique ID of the list. |
