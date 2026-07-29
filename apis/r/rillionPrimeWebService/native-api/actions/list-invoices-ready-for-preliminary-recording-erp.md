# List Invoices Ready for Preliminary Recording ERP with Rillion Prime Web Service

List invoices ready for preliminary recording for one ERP.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Erp` | body | `string` | no | ERP identifier configured in Rillion Prime. |
| `UpdateQueueStatus` | body | `boolean` | yes | When true, returned rows are marked as exported and leave the queue permanently. Keep false to read without consuming. |
| `Company` | body | `list<string>` | no | Company ID to scope the call. |
| `NoOfRows` | body | `string` | no | Maximum number of rows to return. Leave empty for no limit. |
