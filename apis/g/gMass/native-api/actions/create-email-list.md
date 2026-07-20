# Create Email List with GMass

Creates an email list in GMass.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Create Email List](https://api.gmass.co/docs#tag/Lists/operation/Lists_CreateEmailList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listSource` | body | `object` | no |
| `listSource.listSourceSheet` | body | `object` | no |
| `listSource.listSourceSheet.spreadsheetId` | body | `string` | yes |
| `listSource.listSourceSheet.worksheetId` | body | `string` | no |
| `listSource.listSourceSheet.spreadsheetName` | body | `string` | no |
| `listSource.listSourceSheet.worksheetName` | body | `string` | no |
| `KeepDuplicates` | body | `boolean` | no |
| `FilterCriteria` | body | `string` | no |
| `AndOr` | body | `string` | no |
| `UpdateSheet` | body | `boolean` | no |
