# Mass Search And Replace with Ragic

Replaces matching values across multiple Ragic records.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/massOperation/massSearchReplace`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Mass Search And Replace](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Search-And-Replace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes |
| `sheetIndex` | path | `number` | yes |
| `recordId` | query | `number` | no |
| `where` | query | `string` | no |
| `action[0].field` | body | `number` | yes |
| `action[0].valueReplaced` | body | `string` | yes |
| `action[0].valueNew` | body | `string` | yes |
