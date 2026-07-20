# Pipelines GetPipelinesAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/pipelines`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Pipelines GetPipelinesAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-get-pipelines-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports users and stages. |
| `$filter` | query | `string` | no | Filters the results based on a boolean condition. This API only supports filtering for orphaned deployment pipelines. Unsupported filters will return unfiltered results. |
| `$skip` | query | `number` | no | Skips the first n results. Use with top to fetch results beyond the first 5000. |
| `$top` | query | `number` | no | Returns only the first n results. This parameter must be in the range of 1-5000. |
