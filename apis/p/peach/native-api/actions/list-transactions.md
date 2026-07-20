# List Transactions with Peach

Retrieves transaction records from Peach.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/search`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [List Transactions](https://peach-organization.gitbook.io/peach/api-reference/transactions/get-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | body | `date` | no | Start date for retrieving transactions. |
| `endDate` | body | `date` | no | End date for retrieving transactions. |
| `limit` | body | `number` | no | Maximum rows to return. Peach allows up to 1000. |
| `campaignId` | body | `string` | no | Filter results by campaign ID. |
| `paginationKey` | body | `object` | no | Pagination cursor object from a previous response. |
