# List OpenAI Batches with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/batches`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [List OpenAI Batches](https://docs.deepinfra.com/api-reference/files-&-batches/retrieve-openai-batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | yes | Batch pagination cursor from the DeepInfra OpenAI batches API. |
| `limit` | query | `number` | no | Maximum number of batches to return. |
