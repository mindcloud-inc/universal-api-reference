# Create Workspace Tag with BlazeMeter

Creates a workspace tag in BlazeMeter.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/tags`
- **Base URL:** `https://a.blazemeter.com/api/v4`
- **Official documentation:** [Create Workspace Tag](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/tagsCreateTag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | body | `string` | yes |
