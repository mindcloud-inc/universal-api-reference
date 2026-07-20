# List Jobs with Databricks

Retrieves jobs from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.2/jobs/list`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Jobs](https://docs.databricks.com/api/workspace/jobs/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of jobs to return. This value must be greater than 0 and less or equal to 100. The default value is 20. |
| `expand_tasks` | query | `boolean` | no | Whether to include task and cluster details in the response. Note that only the first 100 elements will be shown. Use :method:jobs/get to paginate through all tasks and clusters. |
| `name` | query | `string` | no | A filter on the list based on the exact (case insensitive) job name. |
| `page_token` | query | `string` | no | Use `next_page_token` or `prev_page_token` returned from the previous request to list the next or previous page of jobs respectively. |
