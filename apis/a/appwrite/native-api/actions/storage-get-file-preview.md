# Get file preview with Appwrite

Retrieves the file preview from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/buckets/{bucketId}/files/{fileId}/preview`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get file preview](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | path | `string` | yes | File ID |
| `width` | query | `number` | no | Resize preview image width, Pass an integer between 0 to 4000. |
| `height` | query | `number` | no | Resize preview image height, Pass an integer between 0 to 4000. |
| `gravity` | query | `string` | no | Image crop gravity. Can be one of center,top-left,top,top-right,left,right,bottom-left,bottom,bottom-right |
| `quality` | query | `number` | no | Preview image quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |
| `borderWidth` | query | `number` | no | Preview image border in pixels. Pass an integer between 0 to 100. Defaults to 0. |
| `borderColor` | query | `string` | no | Preview image border color. Use a valid HEX color, no # is needed for prefix. |
| `borderRadius` | query | `number` | no | Preview image border radius in pixels. Pass an integer between 0 to 4000. |
| `opacity` | query | `number` | no | Preview image opacity. Only works with images having an alpha channel (like png). Pass a number between 0 to 1. |
| `rotation` | query | `number` | no | Preview image rotation in degrees. Pass an integer between -360 and 360. |
| `background` | query | `string` | no | Preview image background color. Only works with transparent images (png). Use a valid HEX color, no # is needed for prefix. |
| `output` | query | `string` | no | Output format type (jpeg, jpg, png, gif and webp). |
| `token` | query | `string` | no | File token for accessing this file. |
