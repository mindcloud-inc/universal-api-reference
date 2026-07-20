# Create Attachment with Kanban Tool

## Endpoint

- **Method:** `POST`
- **Path:** `/attachments.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Create Attachment](https://kanbantool.com/developer/api-v3#creating-attachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `file` | yes | File to upload. |
| `attachable` | body | `string` | no | Optional attachable target such as `Board#100000` or `Task#200000`. |
