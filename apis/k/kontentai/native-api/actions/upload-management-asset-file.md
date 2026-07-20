# Upload management asset file with Kontent.ai

Uploads an asset file to Kontent.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/files/:file_name`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Upload management asset file](https://kontent.ai/learn/docs/apis/management-api-v2/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | path | `string` | yes | File name to assign to the uploaded asset file. |
