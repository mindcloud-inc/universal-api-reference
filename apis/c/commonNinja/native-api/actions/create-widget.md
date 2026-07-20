# Create Widget with Common Ninja

Creates a widget in Common Ninja.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [Create Widget](https://developers.commoninja.com/docs/api/widgets/widget-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Widget data payload. |
| `description` | body | `string` | no | The widget description. |
| `modelVersion` | body | `number` | no | The widget data model version. |
| `name` | body | `string` | yes | The name of the widget. |
| `projectId` | body | `string` | no | The related project ID. |
| `status` | body | `string` | yes | The widget status: draft or published. |
| `type` | body | `string` | yes | The widget type to create. |
