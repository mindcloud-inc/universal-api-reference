# Configure Annotation Reply with Dify

Updates annotation reply settings in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/annotation-reply/:action`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Configure Annotation Reply](https://docs.dify.ai/api-reference/annotations/configure-annotation-reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | Annotation reply action to configure. |
| `embedding_provider_name` | body | `string` | yes | Embedding provider name. |
| `embedding_model_name` | body | `string` | yes | Embedding model name. |
| `score_threshold` | body | `number` | yes | Minimum similarity score threshold. |
