# Update Page Break with Clappia

Updates an existing page break in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/updatePageBreak`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Page Break](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `pageIndex` | body | `number` | yes | Zero-based page index to update. |
| `pageMetadata` | body | `object` | yes | Page break metadata such as submit button visibility and custom previous/next labels. |
