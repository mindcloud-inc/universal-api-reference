# Split Sentences with Sapling

Splits text into shorter sentences with Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/rephrase`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Split Sentences](https://sapling.ai/docs/api/rephrase/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Input text to split into shorter sentences. |
