# Create Model Version Config with Scale

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/model_version_configs`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [Create Model Version Config](https://docs.genai.scale.com/model-version-config-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | body | `string` | yes | The target model identifier. |
| `name` | body | `string` | yes | The model version config name. |
