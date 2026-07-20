# Get Render Tags with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/getRenderTags`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Render Tags](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=54)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | body | `string` | yes | A single tag or semicolon-separated list of tags to query. |
| `year` | body | `string` | no | Year to report statistics for. |
| `month` | body | `string` | no | Month number to report statistics for. |
| `nMonths` | body | `string` | no | Number of months of statistics to include, ending at the specified month. |
| `padBlanks` | body | `string` | no | Whether to pad missing periods with zero values. |
