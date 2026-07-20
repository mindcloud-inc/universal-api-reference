# List Boards By Member with Trello

Retrieves boards for a member from Trello.

## Endpoint

- **Method:** `GET`
- **Path:** `members/:id/boards`
- **Base URL:** `https://api.trello.com/1`
- **Official documentation:** [List Boards By Member](https://developer.atlassian.com/cloud/trello/rest/api-group-members/#api-members-id-boards-get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
