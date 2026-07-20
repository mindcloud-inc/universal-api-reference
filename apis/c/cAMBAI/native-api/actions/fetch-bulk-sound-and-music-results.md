# Fetch Bulk Sound and Music Results with CAMB.AI

Retrieves multiple sound and music results from CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/text-to-sound-results`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Fetch Bulk Sound and Music Results](https://docs.camb.ai/api-reference/endpoint/fetch-text-to-sound-runs-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_ids[]` | body | `array<number>` | yes | Two to five completed sound and music run identifiers. |
