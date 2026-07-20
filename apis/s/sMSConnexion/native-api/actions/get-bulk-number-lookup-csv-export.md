# Get Bulk Number Lookup CSV Export with SMS Connexion

Retrieves a bulk lookup export from SMS Connexion as CSV.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/lookup/lookupBulkId/:lookupBulkId/csv`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Bulk Number Lookup CSV Export](https://sms.cx/sms-api-documentation/#operation/ExportNumberLookupReportToCSV)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookupBulkId` | path | `string` | yes | Bulk lookup UUID. |
