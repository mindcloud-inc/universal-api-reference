# Create Discovery Task with Extruct AI

Creates a discovery task in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/discovery_tasks`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Create Discovery Task](https://docs.extruct.ai/api-reference/discover/create-company-discovery-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Natural-language description of companies to find. |
| `desired_num_results` | body | `number` | no | Target number of results for this task. |
| `auto_data_sources` | body | `boolean` | no | Automatically determine the best data sources. |
| `data_sources` | body | `list<string>` | no | Manual data source selection. Accepted values: `LinkedIn`, `Maps`, `Web Search`. Send multiple values as a array. |
| `table` | body | `object` | no | Optional table settings for this discovery task. |
| `table.id` | body | `string` | no | Existing table identifier. |
| `table.run` | body | `boolean` | no | Whether to run the table workflow. |
| `table.columns[]` | body | `array<string>` | no | Table column identifiers. |
| `table.auto_import` | body | `boolean` | no | Whether to auto import task results into the table. |
| `criteria[]` | body | `array<object>` | no | Optional criteria definitions used to score results. |
| `criteria[].key` | body | `string` | no | Criterion key. |
| `criteria[].name` | body | `string` | no | Criterion display name. |
| `criteria[].criterion` | body | `string` | no | Criterion text. |
