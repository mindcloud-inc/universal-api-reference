# List Inboxes with lemlist

Retrieves your inbox conversations from lemlist.

## Endpoint

- **Method:** `GET`
- **Path:** `/inbox`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [List Inboxes](https://developer.lemlist.com/api-reference/endpoints/inbox/get-many-inboxes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | yes | Filter by user ID. |
| `page` | query | `number` | no | Page number to retrieve. |
