# List Pipelines with Databricks

Retrieves pipelines from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.0/pipelines`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Pipelines](https://docs.databricks.com/api/workspace/pipelines/listpipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_token` | query | `string` | no | Page token returned by previous call |
| `max_results` | query | `number` | no | The maximum number of entries to return in a single page. The system may return fewer than max_results events in a response, even if there are more events available. This field is optional. The default value is 25. The maximum value is 100. An error is returned if the value of max_results is greater than 100. |
| `order_by` | query | `list<string>` | no | A list of strings specifying the order of results. Supported order_by fields are id and name. The default is id asc. This field is optional. |
| `filter` | query | `string` | no | Select a subset of results based on the specified criteria. The supported filters are:  * `notebook='<path>'` to select pipelines that reference the provided notebook path. * `name LIKE '[pattern]'` to select pipelines with a name that matches pattern. Wildcards are supported, for example: `name LIKE '%shopping%'`  Composite filters are not supported. This field is optional. |
