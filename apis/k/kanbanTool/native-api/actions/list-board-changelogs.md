# List Board Changelogs with Kanban Tool

## Endpoint

- **Method:** `GET`
- **Path:** `/boards/:board_id/changelog.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [List Board Changelogs](https://kanbantool.com/developer/api-v3#listing-boards-changelogs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | path | `number` | yes | Kanban Tool board ID. |
| `before` | query | `number` | no | Only return changelogs with an ID smaller than this value. |
| `after` | query | `number` | no | Only return changelogs with an ID greater than this value. |
| `limit` | query | `number` | no | Maximum number of changelog entries to return. |
