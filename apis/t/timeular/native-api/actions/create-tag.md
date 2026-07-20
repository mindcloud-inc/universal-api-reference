# Create Tag with Timeular

Creates a new tag in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/tags`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Tag](https://developers.early.app/#c23b9b70-b888-43dc-ab74-5cddd3c3e581)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | body | `string` | no |
| `key` | body | `string` | yes |
| `label` | body | `string` | yes |
| `scope` | body | `string` | yes |
