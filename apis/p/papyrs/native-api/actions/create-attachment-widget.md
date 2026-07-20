# Create Attachment Widget with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/page/:page_id/attachment/create/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Create Attachment Widget](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload into the attachment widget. |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
