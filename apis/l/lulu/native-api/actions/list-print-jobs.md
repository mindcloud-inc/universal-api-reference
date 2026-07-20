# List Print Jobs with Lulu

Retrieves print jobs from Lulu.

## Endpoint

- **Method:** `GET`
- **Path:** `/print-jobs/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Print Jobs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | Number of print jobs to return per page. |
| `search` | query | `string` | no | Search by Lulu print job fields. |
| `status` | query | `string` | no | Filter print jobs by status. |
