# Get Custom Print Report with Ragic

Retrieves a custom print report from Ragic.

## Endpoint

- **Method:** `GET`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId.carbone`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Get Custom Print Report](https://www.ragic.com/docs/api/en/#tag/reading-exports/operation/getRecordCarbone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `recordId` | path | `number` | yes | The record ID from the Ragic record URL. |
| `fileFormat` | query | `string` | yes | The export file format. Supported values are `pdf`, `png`, and `docx`. |
| `ragicCustomPrintTemplateId` | query | `number` | yes | The Custom Print Report template ID copied from a Ragic download URL. |
| `fileNameRefDomainId` | query | `number` | no | Optional field ID whose value will be used as the downloaded file name. |
