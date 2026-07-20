# Add Datasourcefile Text Blob with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/datasource/:datasource_id/text_blob`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Add Datasourcefile Text Blob](https://docs.insighto.ai/api-reference/data-source/add-datasourcefile-text-blob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasource_id` | path | `string` | yes | The UUID id of the datasource. |
| `ds_type` | query | `list<string>` | yes | Datasource type for the text blob. Accepted values: `doc`, `http`, `image`, `pdf`, `text_blob`, `text_image`, `tool`. |
