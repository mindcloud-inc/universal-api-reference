# Untrash Thread with Google Mail

Removes a Gmail thread from trash.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/:id/untrash`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Untrash Thread](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/untrash)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gmail thread ID to restore from trash. |
