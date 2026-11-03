# Start Product Export with Rithum for Brands

## Endpoint

- **Method:** `POST`
- **Path:** `ProductExport`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Start Product Export](https://api.channeladvisor.com/apidocs#tag/ProductExport/operation/ProductExport.ExportFile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | query | `list<number>` | no | Leave empty to use the profile associated with the access token. |
| `fields` | body | `string` | no | Comma-separated field names to include. Leave empty to export all fields. Send multiple values as a string separated by `,`. |
| `$filter` | query | `string` | no | Product filter expression, for example ProfileID eq 12345. |
