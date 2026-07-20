# Trash Thread with Google Mail

Moves a Gmail thread to trash.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/:id/trash`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Trash Thread](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/trash)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gmail thread ID to move to trash. |
