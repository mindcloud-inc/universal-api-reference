# List Invoices for Update in ERP with Rillion Prime Web Service

List invoices with updated account coding that should be updated in the ERP.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdateQueueStatus` | body | `boolean` | yes | When true, returned rows are marked as exported and leave the queue permanently. Keep false to read without consuming. |
| `Company` | body | `list<string>` | no | Company ID to scope the call. |
| `NoOfRows` | body | `string` | no | Maximum number of rows to return. Leave empty for no limit. |
