# Import Transactions with Sales Cookie

Imports transaction CSV data into Sales Cookie.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/ImportData`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Import Transactions](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-full-transaction-import-rest-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionBatchId` | body | `string` | yes | Batch ID returned by Prepare Full Transaction Import and sent in X-TransactionBatchId. |
| `csvContent` | body | `string` | yes | CSV content including the header row in the same order as the mapping XML. |
