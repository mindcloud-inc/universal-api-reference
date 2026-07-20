# List Notebooks with Datadog

Retrieves notebooks from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/notebooks`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List Notebooks](https://docs.datadoghq.com/api/latest/notebooks/#get-all-notebooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_handle` | query | `string` | no | Return notebooks created by this author handle. |
| `exclude_author_handle` | query | `string` | no | Exclude notebooks by author handle. |
| `count` | query | `number` | no | Number of notebooks to return. |
| `start` | query | `number` | no | Index of the first notebook to return. |
| `sort_field` | query | `string` | no | Field to sort notebooks by. |
| `sort_dir` | query | `string` | no | Direction for notebook sorting. |
| `query` | query | `string` | no | Search notebooks by name or author handle. |
| `include_cells` | query | `boolean` | no | Whether to include cells and global time in notebook results. |
| `is_template` | query | `boolean` | no | Return only template notebooks when true. |
| `type` | query | `string` | no | Notebook metadata type filter. |
