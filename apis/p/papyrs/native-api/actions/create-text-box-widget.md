# Create Text Box Widget with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/page/:page_id/paragraph/create/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Create Text Box Widget](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Optional format for widget.val. Defaults to html. |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
| `widget.val` | body | `string` | yes | The text or HTML value for the widget. |
