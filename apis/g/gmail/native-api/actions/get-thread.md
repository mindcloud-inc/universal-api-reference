# Get Thread with Google Mail

Retrieves a Gmail thread.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Get Thread](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | (Required) The ID of the thread to retrieve. |
| `fields` | query | `string` | no | e.g. historyId,messages(id,labelIds,internalDate,snippet,payload/headers) |
| `format` | query | `list<string>` | no | — |
| `metadataHeaders` | query | `string` | no | Send multiple values as a array. |
