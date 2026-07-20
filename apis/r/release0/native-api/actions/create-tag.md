# Create Tag with Release0

Creates a new tag in Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tags`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Create Tag](https://docs.release0.com/workspace/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The tag color. |
| `name` | body | `string` | yes | The tag name. |
| `workspaceId` | body | `string` | yes | The workspace ID that owns the tag. |
