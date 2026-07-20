# Delete Draft with Google Mail

Deletes a Gmail draft permanently.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/drafts/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Delete Draft](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Draft ID to delete. |
