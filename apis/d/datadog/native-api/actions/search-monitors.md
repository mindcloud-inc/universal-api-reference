# Search Monitors with Datadog

Finds monitors in Datadog by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/monitor/search`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Search Monitors](https://docs.datadoghq.com/api/latest/monitors/#monitors-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to start monitor search pagination from. |
| `per_page` | query | `number` | no | Number of monitor search results to return per page. |
| `query` | query | `string` | no | Monitor search query from the Datadog Manage Monitors page URL, for example type:metric status:alert. |
| `sort` | query | `string` | no | Sort order in the form field,direction such as name,asc or status,desc. |
