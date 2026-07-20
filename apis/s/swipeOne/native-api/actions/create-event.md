# Create Event with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/events`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Event](https://docs.swipeone.com/en/articles/10545660-events#h_29d9bc4044)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes |
| `type` | body | `string` | yes |
| `contact` | body | `object` | no |
| `properties` | body | `object` | no |
| `createdBy` | body | `object` | no |
