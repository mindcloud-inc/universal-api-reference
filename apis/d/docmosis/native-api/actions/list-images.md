# List Images with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/listImages`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Images](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=49)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | body | `string` | no | Optional starting folder path. If omitted, all images are listed. |
| `includeSubFolders` | body | `string` | no | Whether to include images within subfolders. Defaults to true. |
