# Update Widget with Common Ninja

Updates a widget in Common Ninja.

## Endpoint

- **Method:** `PUT`
- **Path:** `/widgets/:id`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [Update Widget](https://developers.commoninja.com/docs/api/widgets/widget-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Updated widget data payload. |
| `description` | body | `string` | no | The updated widget description. |
| `id` | path | `string` | yes | The widget ID. |
| `name` | body | `string` | no | The updated widget name. |
| `status` | body | `string` | no | The updated widget status: draft or published. |
