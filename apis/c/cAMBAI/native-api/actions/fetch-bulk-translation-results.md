# Fetch Bulk Translation Results with CAMB.AI

Retrieves multiple translation results from CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/translation-results`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Fetch Bulk Translation Results](https://docs.camb.ai/api-reference/endpoint/fetch-translation-runs-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_ids[]` | body | `array<number>` | yes | Two to five completed translation run identifiers. |
