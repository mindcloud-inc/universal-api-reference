# Set Attachment Mode with Kanban Tool

## Endpoint

- **Method:** `PATCH`
- **Path:** `/attachments/:attachment_id/set_mode.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Set Attachment Mode](https://kanbantool.com/developer/api-v3#attachments-mode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `number` | yes | Kanban Tool attachment ID. |
| `attachable` | query | `string` | yes | Attachable target such as `Board#100000` or `Task#200000`. |
| `mode` | query | `number` | yes | Mode flags: `0` none, `1` pinned, `2` cover, `3` pinned and cover. |
