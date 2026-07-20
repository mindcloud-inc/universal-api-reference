# Create Event Definition with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/event-definitions`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Event Definition](https://docs.swipeone.com/en/articles/10358929-how-to-create-custom-event-definition-events#h_f97ca0d3fc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `label` | body | `string` | yes |
| `properties[]` | body | `array<object>` | yes |
| `recordSummary` | body | `boolean` | yes |
