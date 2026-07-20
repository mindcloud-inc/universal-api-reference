# Create Design Export Job with Canva

Creates a design export job in Canva.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/exports`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Create Design Export Job](https://www.canva.dev/docs/connect/api-reference/exports/create-design-export-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `design_id` | body | `string` | yes | The design ID. |
| `format` | body | `object` | yes | Details about the desired export format. |
| `format.type` | body | `list<string>` | yes | The export file format type. Accepted values: `gif`, `jpg`, `mp4`, `pdf`, `png`, `pptx`. |
| `format.export_quality` | body | `list<string>` | no | Specifies the export quality of the design. Accepted values: `pro`, `regular`. |
| `format.quality` | body | `string` | no | The media quality setting for JPG or MP4 exports. |
| `format.size` | body | `list<string>` | no | The paper size of the export PDF file. Accepted values: `a3`, `a4`, `legal`, `letter`. |
| `format.height` | body | `number` | no | The export height in pixels. |
| `format.width` | body | `number` | no | The export width in pixels. |
| `format.pages[]` | body | `array<number>` | no | Page numbers to export from a multi-page design. |
| `format.lossless` | body | `boolean` | no | Whether to export the PNG without compression. |
| `format.transparent_background` | body | `boolean` | no | Whether to export the PNG with a transparent background. |
| `format.as_single_image` | body | `boolean` | no | Whether to merge a multi-page PNG export into a single image. |
