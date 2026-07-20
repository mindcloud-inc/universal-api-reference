# Send Attachment with Synchroteam

Creates an attachment in Synchroteam for a job or customer.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/Attachments/Send`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Send Attachment](https://api.synchroteam.com/v2/#send-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | yes | Request body payload for sending an attachment (fileName, fileData base64, and linked entity) per docs. |
