# Upload Transactions Csv with Sales Cookie

Uploads transaction CSV data to Sales Cookie.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/UploadTransactions`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Upload Transactions Csv](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-csv-upload-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/csv` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionBatchId` | query | `string` | yes | Configuration hash from the provider upload URL. |
| `csvContent` | body | `string` | yes | CSV content to upload, including the header row. |
