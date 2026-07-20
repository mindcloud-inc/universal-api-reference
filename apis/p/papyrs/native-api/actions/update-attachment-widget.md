# Update Attachment Widget with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/page/:page_id/attachment/update/:widget_id/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Update Attachment Widget](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to add to the existing attachment widget. |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
| `widget_id` | path | `string` | yes | The Papyrs widget ID on the page. |
