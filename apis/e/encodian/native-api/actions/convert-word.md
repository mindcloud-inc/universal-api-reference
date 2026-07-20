# Convert Word with Encodian

Converts a Word document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertWord`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert Word](https://support.encodian.com/hc/en-gb/articles/360015616117)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `outputFormat` | body | `string` | yes |
| `filename` | body | `string` | yes |
| `fileContent` | body | `string` | yes |
| `pageOrientation` | body | `string` | no |
| `pageSize` | body | `string` | no |
| `removeMarkup` | body | `boolean` | no |
| `showRevisionsInBalloons` | body | `string` | no |
| `trackedChangesInsertedTextColor` | body | `string` | no |
| `trackedChangesDeletedTextColor` | body | `string` | no |
| `trackedChangesMovedToTextColor` | body | `string` | no |
| `trackedChangesMovedFromTextColor` | body | `string` | no |
| `trackedChangesCommentsColor` | body | `string` | no |
| `timeZone` | body | `string` | no |
| `cultureName` | body | `string` | no |
| `htmlVersion` | body | `string` | no |
| `exportListLabels` | body | `string` | no |
| `generateBookmarks` | body | `boolean` | no |
| `customProperties` | body | `string` | no |
| `pdfACompliant` | body | `boolean` | no |
| `pdfAComplianceLevel` | body | `string` | no |
| `convertToPdfForm` | body | `boolean` | no |
| `enableOpenType` | body | `boolean` | no |
| `pageIndex` | body | `number` | no |
| `compression` | body | `string` | no |
