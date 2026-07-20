# Update Card Property with Superthread

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:team_id/cards/:card_id`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Update Card Property](https://superthread.com/docs/api-docs/cards/update-a-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | no | Card title. |
| `card_id` | path | `string` | yes | Card ID to update. |
