# Update Heading Widget with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/page/:page_id/heading/update/:widget_id/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Update Heading Widget](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Optional format for widget.val. Defaults to html. |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
| `widget_id` | path | `string` | yes | The Papyrs widget ID on the page. |
| `widget.val` | body | `string` | yes | The updated text or HTML value for the widget. |
