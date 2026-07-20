# Create Tag with EARLY

Creates a new tag in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/tags`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Tag](https://developers.early.app/#c23b9b70-b888-43dc-ab74-5cddd3c3e581)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | External tag key. |
| `label` | body | `string` | yes | Tag label. |
| `scope` | body | `string` | yes | Tag scope. |
| `folderId` | body | `string` | yes | Folder ID. |
