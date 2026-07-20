# Get Video Comments with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/:id`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Video Comments](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token for the next chunk of comments. |
| `id` | path | `string` | yes | Video ID to fetch comments for. |
| `sort_by` | query | `string` | no | Comment sort order: top or new. |
| `source` | query | `string` | no | Comment source: youtube or reddit. |
