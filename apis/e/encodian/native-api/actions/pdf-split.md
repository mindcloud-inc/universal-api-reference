# PDF Split with Encodian

Splits a PDF document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/SplitDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Split](https://support.encodian.com/hc/en-gb/articles/360002953277)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The filename of the source PDF document including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the source PDF document. |
| `SplitByType` | body | `string` | yes | Set the option for splitting the PDF document. |
| `SplitConfiguration` | body | `string` | yes | Specify the split configuration aligned to the selected split by type option. |
| `EnableBookmarkFilenames` | body | `boolean` | no | Append the bookmark name value to the filename when splitting by bookmark level. |
