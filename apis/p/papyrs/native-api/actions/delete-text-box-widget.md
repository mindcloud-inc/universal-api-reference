# Delete Text Box Widget with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/page/:page_id/paragraph/delete/:widget_id/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Delete Text Box Widget](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | The Papyrs page ID. |
| `widget_id` | path | `string` | yes | The Papyrs widget ID on the page. |
