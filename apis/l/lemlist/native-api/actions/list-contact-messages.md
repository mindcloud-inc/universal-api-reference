# List Contact Messages with lemlist

Retrieves contact messages from lemlist inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inbox/:contactId`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [List Contact Messages](https://developer.lemlist.com/api-reference/endpoints/inbox/get-contact-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The unique identifier of the contact. |
| `userId` | query | `string` | no | Required when `markAsRead` is provided so lemlist can resolve the viewing user. |
| `skip` | query | `number` | no | Number of items to skip. |
| `markAsRead` | query | `boolean` | no | When true, marks the conversation as read. If provided, also send `userId`. |
