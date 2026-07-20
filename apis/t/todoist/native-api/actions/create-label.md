# Create Label with Todoist

Creates a new label in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/labels`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Create Label](https://developer.todoist.com/api/v1/#tag/Labels/operation/create_label_api_v1_labels_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Label name. |
| `order` | body | `number` | no | Custom label order value. |
| `color` | body | `string` | no | Label color name or legacy color code. |
| `is_favorite` | body | `boolean` | no | Whether the label should be marked as favorite. |
