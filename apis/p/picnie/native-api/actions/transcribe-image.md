# Transcribe Image with Picnie

Retrieves OCR text from an image in Picnie.

## Endpoint

- **Method:** `POST`
- **Path:** `/transcribe-image`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Transcribe Image](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID for the OCR operation. |
| `image_url` | body | `string` | yes | Image URL to transcribe. |
| `method` | body | `string` | yes | OCR method. The docs example uses Original. |
| `language` | body | `string` | yes | OCR language. The docs example uses Original. |
