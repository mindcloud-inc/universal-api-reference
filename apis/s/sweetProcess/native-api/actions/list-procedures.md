# List Procedures with SweetProcess

Retrieves procedures from SweetProcess.

## Endpoint

- **Method:** `GET`
- **Path:** `/procedures/`
- **Base URL:** `https://www.sweetprocess.com/api/v1`
- **Official documentation:** [List Procedures](https://www.sweetprocess.com/kb/8LBTequD/article/y9C9fKdyD/integrating-sweetprocess-with-chatgpt-via-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Full-text search for procedures. |
| `team_id` | query | `number` | no | Filter procedures within the given team. |
| `tag` | query | `string` | no | Comma-separated tag names to filter procedures. |
| `policy_id` | query | `number` | no | Filter procedures attached to the given policy. |
| `visible_to_user` | query | `string` | no | Filter procedures visible to both the current user and the referenced user URL. |
