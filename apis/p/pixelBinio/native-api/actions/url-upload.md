# Upload Asset From URL with PixelBin.io

Creates a new uploaded file in PixelBin.io from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/upload/url`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Upload Asset From URL](https://www.pixelbin.io/docs/api/upload-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access` | body | `string` | no | Access level for the uploaded asset. |
| `filenameOverride` | body | `boolean` | no | Whether to append a unique suffix when a matching file name already exists. |
| `metadata` | body | `object` | no | Metadata object to associate with the upload. |
| `name` | body | `string` | no | Name for the uploaded asset. |
| `overwrite` | body | `boolean` | no | Whether to overwrite an existing asset with the same name. |
| `path` | body | `string` | no | Path where the uploaded asset should be stored. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the upload. |
| `url` | body | `string` | yes | Source URL for the asset to upload into PixelBin. |
