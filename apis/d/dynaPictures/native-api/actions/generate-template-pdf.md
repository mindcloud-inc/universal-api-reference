# Generate Template PDF with DynaPictures

Creates a PDF from a DynaPictures template.

## Endpoint

- **Method:** `POST`
- **Path:** `/designs/:uid`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Generate Template PDF](https://dynapictures.com/docs/#pdf-generation)

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
| `index` | body | `number` | no | Index of the template page to render. |
| `layers[]` | body | `array<object>` | no | Layer customizations for the page. |
| `metadata` | body | `string` | no | Custom metadata to store on the generated PDF. |
| `name` | body | `string` | no | Name of the layer to customize. |
| `opacity` | body | `number` | no | Layer opacity from 0 to 1. |
| `pages[]` | body | `array<object>` | no | Pages to render for the PDF. |
| `text` | body | `string` | no | Text rendered in the layer. |
| `UID` | path | `string` | yes | UID of the multipage template to render as PDF. |
