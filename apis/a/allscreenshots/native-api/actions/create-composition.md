# Create Composition with Allscreenshots

Creates a single image from multiple screenshots in Allscreenshots.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/screenshots/compose`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Create Composition](https://docs.allscreenshots.com/api-reference/compose)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `captures[]` | body | `array<object>` | no | Capture-mode composition input with multiple URLs and optional labels. |
| `url` | body | `string` | no | Variants-mode source URL for a composition request. |
| `variants[]` | body | `array<object>` | no | Variants-mode device or configuration list. |
| `output` | body | `object` | no | Composition layout and styling options. |
