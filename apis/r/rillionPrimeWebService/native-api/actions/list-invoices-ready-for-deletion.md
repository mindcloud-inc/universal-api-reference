# List Invoices Ready for Deletion with Rillion Prime Web Service

List invoices marked ready for deletion in the Prime invoice queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdateQueueStatus` | body | `boolean` | yes | When true, returned rows are marked as exported and leave the queue permanently. Keep false to read without consuming. |
| `Company` | body | `list<string>` | no | Company ID to scope the call. |
| `NoOfRows` | body | `string` | no | Maximum number of rows to return. Leave empty for no limit. |
