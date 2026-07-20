# Create Mention with EARLY

Creates a new mention in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/mentions`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Mention](https://developers.early.app/#23643fec-12a2-4fa2-8c72-d57f7fe96682)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | External mention key. |
| `label` | body | `string` | yes | Mention label. |
| `scope` | body | `string` | yes | Mention scope. |
| `folderId` | body | `string` | yes | Folder ID. |
