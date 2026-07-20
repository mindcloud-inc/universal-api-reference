# Create Shot Attachment with Dribbble

## Endpoint

- **Method:** `POST`
- **Path:** `/shots/:shot/attachments`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Create Shot Attachment](https://developer.dribbble.com/v2/attachments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shot` | path | `number` | yes | The Dribbble shot ID. |
| `file` | body | `file` | yes | The attachment file to upload. |
