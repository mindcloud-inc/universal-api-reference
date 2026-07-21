# Update Workspace Tag with BlazeMeter

Updates a workspace tag in BlazeMeter.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workspaces/:workspaceId/tags/:tagId`
- **Base URL:** `https://a.blazemeter.com/api/v4`
- **Official documentation:** [Update Workspace Tag](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/tagsUpdateTag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tagId` | path | `string` | yes |
| `label` | body | `string` | yes |
