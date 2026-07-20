# Update Label with Google Mail

Updates a Gmail label.

## Endpoint

- **Method:** `PUT`
- **Path:** `/labels/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Update Label](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Label ID to update. |
