# Get Bulk Number Lookup XLSX Export with SMS Connexion

Retrieves a bulk lookup export from SMS Connexion as XLSX.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/lookup/lookupBulkId/:lookupBulkId/xlsx`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Bulk Number Lookup XLSX Export](https://sms.cx/sms-api-documentation/#operation/ExportNumberLookupReportToXLSX)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookupBulkId` | path | `string` | yes | Bulk lookup UUID. |
