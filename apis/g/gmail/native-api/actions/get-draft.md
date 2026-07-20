# Get Draft with Google Mail

Retrieves a Gmail draft.

## Endpoint

- **Method:** `GET`
- **Path:** `/drafts/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Get Draft](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Draft ID to fetch. |
