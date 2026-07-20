# Get Enterprise Tree Count by Date Range with Digital Humani

Retrieves an enterprise tree count from Digital Humani by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/enterprise/:id/treeCount`
- **Base URL:** `https://api.digitalhumani.com`
- **Official documentation:** [Get Enterprise Tree Count by Date Range](https://docs.digitalhumani.com/#apitree_get_enterprise_count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | End date in YYYY-MM-DD format. |
| `startDate` | query | `string` | yes | Start date in YYYY-MM-DD format. |
