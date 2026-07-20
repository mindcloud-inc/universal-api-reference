# Reprocess Source with Graphor

Updates an existing source in Graphor with a new partition method.

## Endpoint

- **Method:** `POST`
- **Path:** `/reprocess`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Reprocess Source](https://docs.graphorlm.com/api-reference/sources/process)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | The unique identifier of the source to reprocess. |
| `method` | body | `string` | no | Optional partition method to use for reprocessing, such as fast, balanced, accurate, vlm, or agentic. |
