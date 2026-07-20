# Create Comment with Sifter

Creates a new comment on a Sifter issue.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/issues/:issue_id`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [Create Comment](https://sifterapp.com/developer/documentation/comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The comment body. |
| `internal` | body | `boolean` | no | Set true to make the comment visible only to the primary organization. |
| `issue_id` | path | `number` | yes | The Sifter issue ID. |
| `project_id` | path | `number` | yes | The Sifter project ID. |
