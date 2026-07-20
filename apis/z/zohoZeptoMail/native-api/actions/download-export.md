# Download Export with Zoho ZeptoMail

Downloads a log export from Zoho ZeptoMail.

## Endpoint

- **Method:** `GET`
- **Path:** `:exportType/exports/:exportId/download`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Download Export](https://www.zoho.com/zeptomail/help/api/download-exports.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exportType` | path | `string` | yes | Export category to download from. |
| `exportId` | path | `string` | yes | Export job identifier. |
