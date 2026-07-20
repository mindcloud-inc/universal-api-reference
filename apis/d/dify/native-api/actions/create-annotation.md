# Create Annotation with Dify

Creates a new annotation in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/annotations`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Create Annotation](https://docs.dify.ai/api-reference/annotations/create-annotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question` | body | `string` | yes | Annotation question. |
| `answer` | body | `string` | yes | Annotation answer. |
