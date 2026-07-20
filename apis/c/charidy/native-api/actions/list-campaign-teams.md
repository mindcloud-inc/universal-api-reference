# List Campaign Teams with Charidy

Retrieves teams for a campaign from Charidy.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaign/:campaignId/teams`
- **Base URL:** `https://api.charidy.com`
- **Official documentation:** [List Campaign Teams](https://documenter.getpostman.com/view/1118680/S1a4WS4g)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The campaign ID whose teams to list. |
| `grouped` | query | `boolean` | no | Whether to return grouped teams. |
| `offset` | query | `number` | no | Return teams starting after this offset. |
| `limit` | query | `number` | no | Maximum number of teams to return. |
| `sort` | query | `string` | no | Sort teams by the requested field and direction. |
| `parent_team_id` | query | `number` | no | Filter results by parent team ID when applicable. |
| `parent_only` | query | `boolean` | no | Whether to return only parent teams. |
| `grandparent_only` | query | `boolean` | no | Whether to return only grandparent teams. |
| `skip_parent` | query | `boolean` | no | Whether to exclude parent teams from the results. |
