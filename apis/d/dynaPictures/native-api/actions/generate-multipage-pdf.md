# Generate Multipage PDF with DynaPictures

Creates a PDF from a multipage DynaPictures template.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Generate Multipage PDF](https://dynapictures.com/docs/#multipage-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backgroundColor` | body | `string` | no | Background color of the layer. |
| `borderColor` | body | `string` | no | Border color of the layer. |
| `borderRadius` | body | `string` | no | Border radius of the layer. |
| `borderWidth` | body | `string` | no | Border width of the layer. |
| `color` | body | `string` | no | Text color for the layer. |
| `imageAlignH` | body | `string` | no | Horizontal alignment when imagePosition is align. |
| `imageAlignV` | body | `string` | no | Vertical alignment when imagePosition is align. |
| `imageEffect` | body | `string` | no | CSS filter-style effect applied to the image. |
| `imagePosition` | body | `string` | no | Positioning mode for the image inside its container. |
| `imageUrl` | body | `string` | no | Image used for an image layer. |
| `layers[]` | body | `array<object>` | no | Layer customizations for the page. |
| `metadata` | body | `string` | no | Custom metadata for generated PDF pages. |
| `metadata` | body | `string` | no | Custom metadata for this page. |
| `name` | body | `string` | no | Name of the layer to customize. |
| `opacity` | body | `number` | no | Layer opacity from 0 to 1. |
| `pages[]` | body | `array<object>` | yes | Pages to render in the batch PDF. |
| `templateId` | body | `string` | no | Default template ID for batch pages. |
| `templateId` | body | `string` | no | Template ID to use for this page. |
| `text` | body | `string` | no | Text rendered in the layer. |
