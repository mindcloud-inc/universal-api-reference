# Create a Tax Line with Veryfi

Creates a tax line in a document in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/documents/:document_id/tax-lines`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Create a Tax Line](https://docs.veryfi.com/api/create-a-tax-line/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_region[]` | body | `array<number>` | yes | The base amount of the tax applied. number Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `order` | body | `number` | yes | The arrangement of tax lines in relation to each other. |
