# Modify Thread Labels with Google Mail

Updates labels on a Gmail thread.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/:id/modify`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Modify Thread Labels](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/modify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gmail thread ID to modify labels for. |
