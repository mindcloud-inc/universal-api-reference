# Upload Image with Printify

Uploads an image to Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/images.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Upload Image](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Name for the uploaded image file. |
| `url` | body | `string` | yes | Public URL for the image to upload. |
