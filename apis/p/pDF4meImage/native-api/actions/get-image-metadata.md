# Get Image Metadata with PDF4me Image

Retrieves metadata for an image in PDF4me Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetImageMetadata`
- **Base URL:** `https://api.pdf4me.com/api/v2`
- **Official documentation:** [Get Image Metadata](https://docs.pdf4me.com/url-api-tester/get-image-metadata/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docContent` | body | `string` | yes | Base64-encoded PNG or JPG image content. |
| `docName` | body | `string` | yes | File name for the uploaded image, including the extension. |
| `imageType` | body | `string` | no | Optional image type such as PNG or JPG when the provider needs it. |
