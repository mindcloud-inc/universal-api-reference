# Replace Card Description with Superthread

## Endpoint

- **Method:** `PUT`
- **Path:** `/:team_id/cards/:card_id/content`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Replace Card Description](https://superthread.com/docs/api-docs/cards/replace-a-card-description)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `card_id` | path | `string` | yes | Card ID to update. |
| `content` | body | `string` | yes | Full card description content. |
