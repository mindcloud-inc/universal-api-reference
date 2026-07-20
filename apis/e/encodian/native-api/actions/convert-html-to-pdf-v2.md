# Convert HTML To PDF V2 with Encodian

Converts HTML to PDF in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/HtmlToPDFV2`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert HTML To PDF V2](https://support.encodian.com/hc/en-gb/articles/16421778005020)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `htmlData` | body | `string` | no |
| `htmlUrl` | body | `string` | no |
| `filename` | body | `string` | no |
| `fileContent` | body | `string` | no |
| `pageOrientation` | body | `string` | no |
| `pageSize` | body | `string` | no |
| `createBookmarks` | body | `boolean` | no |
| `createTableOfContents` | body | `boolean` | no |
| `cssType` | body | `string` | no |
| `decodeHtmlData` | body | `boolean` | no |
| `delay` | body | `number` | no |
| `enableHyperlinks` | body | `boolean` | no |
| `enableJavaScript` | body | `boolean` | no |
| `topMargin` | body | `number` | no |
| `bottomMargin` | body | `number` | no |
| `rightMargin` | body | `number` | no |
| `leftMargin` | body | `number` | no |
| `pageRotation` | body | `string` | no |
| `scale` | body | `number` | no |
| `viewPort` | body | `string` | no |
