# List Reports with Action1

Retrieves all enterprise reports from Action1.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/all`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Reports](https://app.action1.com/apidocs/#/Reports.%20Report%20Definition%20Objects/reports_all_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subtree` | query | `list` | no | Specify if you want to query the entire report subtree. Accepted values: `0`, `1`. |
