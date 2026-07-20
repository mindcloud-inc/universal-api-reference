# Update Tag with TxtSync

Updates an existing tag in TxtSync.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:id`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Update Tag](https://docs.txtsync.com/#update-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Tag identifier. |
| `Name` | body | `string` | yes | Updated unique tag name. |
