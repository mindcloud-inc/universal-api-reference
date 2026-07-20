# Create Tag with Timely

Creates a tag in Timely.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.1/{account_id}/labels`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Create Tag](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `label.name` | body | `string` | yes | — |
| `label.emoji` | body | `string` | no | — |
| `label.parent_id` | body | `string` | no | — |
| `label.sequence` | body | `string` | no | — |
| `label.active` | body | `string` | no | — |
| `label.external_id` | body | `string` | no | — |
