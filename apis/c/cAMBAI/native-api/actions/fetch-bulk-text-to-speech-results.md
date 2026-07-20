# Fetch Bulk Text-to-Speech Results with CAMB.AI

Retrieves multiple text-to-speech results from CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/tts-results`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Fetch Bulk Text-to-Speech Results](https://docs.camb.ai/api-reference/endpoint/fetch-tts-runs-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_ids[]` | body | `array<number>` | yes | Two to five completed text-to-speech run identifiers. |
