# Create Mention with Timeular

Creates a new mention in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/mentions`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Mention](https://developers.early.app/#23643fec-12a2-4fa2-8c72-d57f7fe96682)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | body | `string` | no |
| `key` | body | `string` | yes |
| `label` | body | `string` | yes |
| `scope` | body | `string` | yes |
