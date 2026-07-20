# List Contacts with ClickSend SMS

Retrieves contacts from a ClickSend SMS list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/lists/:list_id/contacts`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [List Contacts](https://developers.clicksend.com/docs/contacts/lists/other/create-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `number` | yes | List identifier. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Items per page. |
| `updated_after` | query | `number` | no | Unix timestamp lower bound. |
