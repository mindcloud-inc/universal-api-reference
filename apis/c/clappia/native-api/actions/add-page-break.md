# Add Page Break with Clappia

Creates a new page break in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/addPageBreak`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add Page Break](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `pageIndex` | body | `number` | yes | Zero-based page index where the page break should be inserted. |
| `sectionIndex` | body | `number` | yes | Zero-based section index after which the page break should be inserted. |
| `pageMetadata` | body | `object` | no | Optional page break metadata such as submit button visibility and custom previous/next labels. |
