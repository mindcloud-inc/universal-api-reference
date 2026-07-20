# Export Map Comments with Felt

Retrieves exported map comments from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/maps/:mapId/comments/export`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Export Map Comments](https://developers.felt.com/rest-api/api-reference/comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map to export comments from. |
| `format` | query | `list` | no | The export format for the comments. Accepted values: `0`, `1`, `2`. |
