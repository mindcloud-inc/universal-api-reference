# Generate Image with DynaPictures

Creates an image from a DynaPictures template.

## Endpoint

- **Method:** `POST`
- **Path:** `/designs/:uid`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Generate Image](https://dynapictures.com/docs/#image-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backgroundColor` | body | `string` | no | Background color of the layer. |
| `borderColor` | body | `string` | no | Border color of the layer. |
| `borderRadius` | body | `string` | no | Border radius of the layer. |
| `borderWidth` | body | `string` | no | Border width of the layer. |
| `chartColor` | body | `string` | no | Color of the chart. |
| `chartDataLabels[]` | body | `array<string>` | no | Labels shown on the chart axis. |
| `chartDataValues[]` | body | `array<number>` | no | Numeric values for the chart data series. |
| `chartLabelColor` | body | `string` | no | Color of chart labels. |
| `color` | body | `string` | no | Text color for the layer. |
| `format` | body | `string` | no | Output image format. |
| `imageAlignH` | body | `string` | no | Horizontal alignment when imagePosition is align. |
| `imageAlignV` | body | `string` | no | Vertical alignment when imagePosition is align. |
| `imageEffect` | body | `string` | no | CSS filter-style effect applied to the image. |
| `imagePosition` | body | `string` | no | Positioning mode for the image inside its container. |
| `imageUrl` | body | `string` | no | Image used for an image layer. |
| `metadata` | body | `string` | no | Custom metadata to store on the generated image. |
| `name` | body | `string` | no | Name of the layer to customize. |
| `opacity` | body | `number` | no | Layer opacity from 0 to 1. |
| `params[]` | body | `array<object>` | no | Layer parameters to customize during image generation. |
| `text` | body | `string` | no | Text rendered in the layer. |
| `UID` | path | `string` | yes | UID of the template to render. |
