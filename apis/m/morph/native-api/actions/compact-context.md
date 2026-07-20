# Compact Context with Morph

Compacts context with Morph.

## Endpoint

- **Method:** `POST`
- **Path:** `/compact`
- **Base URL:** `https://api.morphllm.com/v1`
- **Official documentation:** [Compact Context](https://docs.morphllm.com/api-reference/endpoint/compact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Text or code context to compact. |
| `query` | body | `string` | no | Optional focus query that tells Morph what context to preserve. |
| `compression_ratio` | body | `number` | no | Fraction of the original input to keep, where lower values compress more aggressively. |
