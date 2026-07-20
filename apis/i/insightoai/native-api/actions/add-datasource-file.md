# Add Datasourcefile with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/datasource/:datasource_id/file`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Add Datasourcefile](https://docs.insighto.ai/api-reference/data-source/add-datasourcefile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasource_id` | path | `string` | yes | The UUID id of the datasource. |
| `ds_type` | query | `list<string>` | yes | Datasource type for the uploaded file. Accepted values: `doc`, `http`, `image`, `pdf`, `text_blob`, `text_image`, `tool`. |
| `datasourcefile_file` | body | `file` | yes | File to upload to the datasource. |
