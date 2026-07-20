# List Transactions By Campaign with Peach

Retrieves transaction records from Peach by campaign ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/search`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [List Transactions By Campaign](https://peach-organization.gitbook.io/peach/api-reference/transactions/get-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign ID to filter transactions. |
| `startDate` | body | `date` | no | Start date for retrieving transactions. |
| `endDate` | body | `date` | no | End date for retrieving transactions. |
| `limit` | body | `number` | no | Maximum rows to return. Peach allows up to 1000. |
| `paginationKey` | body | `object` | no | Pagination cursor object from a previous response. |
