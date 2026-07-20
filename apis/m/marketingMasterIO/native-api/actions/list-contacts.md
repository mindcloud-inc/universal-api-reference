# List Contacts with Marketing Master IO

Retrieves contacts from Marketing Master IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/list`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [List Contacts](https://developers.marketingmaster.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id` | query | `string` | no | Filter contacts by contact book ID. |
| `tag` | query | `string` | no | Filter contacts by tag ID. |
