# Detach Attachment with Kanban Tool

## Endpoint

- **Method:** `DELETE`
- **Path:** `/attachments/:attachment_id/detach.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Detach Attachment](https://kanbantool.com/developer/api-v3#detaching-attachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `number` | yes | Kanban Tool attachment ID. |
| `attachable` | body | `string` | no | Optional attachable target such as `Board#100000` or `Task#200000`. |
