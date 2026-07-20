# Delete Label with Google Mail

Deletes a Gmail label.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/labels/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Delete Label](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Label ID to delete. |
