# List Clusters with Databricks

Retrieves clusters from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.1/clusters/list`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Clusters](https://docs.databricks.com/api/workspace/clusters/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_by` | query | `object` | no | Filters to apply to the list of clusters. |
| `page_token` | query | `string` | no | Use next_page_token or prev_page_token returned from the previous request to list the next or previous page of clusters respectively. |
| `page_size` | query | `number` | no | Use this field to specify the maximum number of results to be returned by the server. The server may further constrain the maximum number of results returned in a single page. |
| `sort_by` | query | `object` | no | Sort the list of clusters by a specific criteria. |
