# Get Similar Terms with Sapling

Retrieves similar terms for text from Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/thesaurus`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Get Similar Terms](https://sapling.ai/docs/api/similar-terms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Term to find similar terms for. |
