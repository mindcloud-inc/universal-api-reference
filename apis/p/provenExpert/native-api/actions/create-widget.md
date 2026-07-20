# Create Widget with ProvenExpert

Creates a widget in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/widget/create`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Create Widget](https://developer.provenexpert.com/index_en.html#widget-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.type` | body | `string` | yes | Type of widget to generate. |
| `data.width` | body | `number` | yes | Widget width in pixels. |
| `data.feedback` | body | `number` | no | Whether customer votes should be displayed on the widget. |
