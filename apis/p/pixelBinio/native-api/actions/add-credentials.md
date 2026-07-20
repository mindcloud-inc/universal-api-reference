# Add Transformation Module Credentials with PixelBin.io

Creates new transformation module credentials in PixelBin.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/platform/assets/v1.0/credentials`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Add Transformation Module Credentials](https://www.pixelbin.io/docs/playground/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentials` | body | `object` | yes | Credential object for the selected transformation module. |
| `pluginId` | body | `string` | yes | Unique identifier for the transformation module whose credentials you want to add. |
