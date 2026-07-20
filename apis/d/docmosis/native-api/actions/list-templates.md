# List Templates with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/listTemplates`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Templates](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=37)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | body | `string` | no | Optional folder path to start listing from. |
| `includeSubFolders` | body | `boolean` | no | Whether to include templates inside subfolders. |
| `includeDetail` | body | `boolean` | no | Include template metadata in the listing. |
| `paging` | body | `boolean` | no | Whether to return paged results. |
| `pageToken` | body | `string` | no | Token for the next results page when paging is enabled. |
| `pageSize` | body | `number` | no | Page size when paging is enabled. |
