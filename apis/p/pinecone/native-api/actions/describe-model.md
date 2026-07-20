# Describe Model with Pinecone

Retrieves details for a Pinecone model.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/:model_name`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Describe Model](https://docs.pinecone.io/reference/api/2025-10/inference/describe_model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_name` | path | `string` | yes | The name of the model to describe. |
