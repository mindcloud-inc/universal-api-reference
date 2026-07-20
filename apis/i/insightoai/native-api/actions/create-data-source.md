# Create Data Source with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/datasource`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Create Data Source](https://docs.insighto.ai/api-reference/data-source/create-data-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_type` | body | `list<string>` | yes | Datasource type to create. Accepted values: `doc`, `http`, `image`, `pdf`, `text_blob`, `text_image`, `tool`. |
| `name` | body | `string` | no | Datasource name. |
