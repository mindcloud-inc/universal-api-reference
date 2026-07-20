# Update Transformation Module Credentials with PixelBin.io

Updates transformation module credentials in PixelBin.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service/platform/assets/v1.0/credentials/:pluginId`
- **Base URL:** `https://api.pixelbin.io`
- **Official documentation:** [Update Transformation Module Credentials](https://www.pixelbin.io/docs/playground/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentials` | body | `object` | yes | Replacement credential object for the transformation module. |
| `pluginId` | path | `string` | yes | Transformation module identifier whose credentials you want to update. |
