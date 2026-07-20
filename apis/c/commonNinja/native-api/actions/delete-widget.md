# Delete Widget with Common Ninja

Deletes a widget from Common Ninja.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/widgets/:id`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [Delete Widget](https://developers.commoninja.com/docs/api/widgets/widget-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The widget ID. |
| `permanent` | query | `boolean` | no | Set true to permanently delete the widget. |
