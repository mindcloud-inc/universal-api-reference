# Create Tag with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/tags`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Tag](https://docs.swipeone.com/en/articles/10545829-tags#h_547ed7132f)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes |
| `label` | body | `string` | yes |
| `color` | body | `string` | no |
