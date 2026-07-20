# Archive Card with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/cards/:card_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Archive Card](https://superthread.com/docs/api-docs/cards/archive-a-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `card_id` | path | `string` | yes | Card ID to archive. |
