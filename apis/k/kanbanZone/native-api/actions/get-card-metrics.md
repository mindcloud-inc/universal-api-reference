# Get Card Metrics with Kanban Zone

Retrieves metrics for a Kanban Zone card.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/:id/metrics`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Get Card Metrics](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Card number or ObjectId. |
| `board` | query | `string` | no | Board public ID for mirrored cards. |
