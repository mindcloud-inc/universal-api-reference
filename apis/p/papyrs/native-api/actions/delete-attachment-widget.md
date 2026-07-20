# Delete Attachment Widget with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/page/:page_id/attachment/delete/:widget_id/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Delete Attachment Widget](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
| `widget_id` | path | `string` | yes | The Papyrs widget ID on the page. |
