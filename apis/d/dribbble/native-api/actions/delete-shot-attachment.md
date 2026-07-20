# Delete Shot Attachment with Dribbble

## Endpoint

- **Method:** `DELETE`
- **Path:** `/shots/:shot/attachments/:id`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Delete Shot Attachment](https://developer.dribbble.com/v2/attachments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shot` | path | `number` | yes | The Dribbble shot ID. |
| `id` | path | `number` | yes | The attachment ID. |
