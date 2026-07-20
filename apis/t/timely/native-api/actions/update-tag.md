# Update Tag with Timely

Updates an existing tag in Timely.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.1/{account_id}/labels/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Update Tag](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Label ID |
| `label.name` | body | `string` | no | — |
| `label.emoji` | body | `string` | no | — |
| `label.parent_id` | body | `string` | no | — |
| `label.sequence` | body | `string` | no | — |
| `label.active` | body | `string` | no | — |
| `label.external_id` | body | `string` | no | — |
