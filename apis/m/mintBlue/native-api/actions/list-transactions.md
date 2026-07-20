# List Transactions with mintBlue

Retrieves transactions from mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [List Transactions](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#listTransactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.project_id` | body | `string` | yes | Project ID filter (required for stable results in this account). |
| `params.startDate` | body | `date` | no | Optional start date filter. |
| `params.endDate` | body | `date` | no | Optional end date filter. |
| `params.sort` | body | `string` | no | Optional sort field. |
| `params.order` | body | `string` | no | Optional sort order (asc\|desc). |
| `params.paginationOptions.limit` | body | `number` | no | Optional pagination limit. |
| `params.paginationOptions.offset` | body | `number` | no | Optional pagination offset. |
