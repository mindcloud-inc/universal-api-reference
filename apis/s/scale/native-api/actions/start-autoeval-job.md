# Start Autoeval Job with Scale

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/autoevals`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [Start Autoeval Job](https://docs.genai.scale.com/autoevals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `libraryName` | body | `string` | yes | The evaluation library name. |
| `modelVersionConfig` | body | `string` | yes | The model version config payload. |
