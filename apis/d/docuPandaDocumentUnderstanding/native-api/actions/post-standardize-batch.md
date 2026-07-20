# Standardize Documents with DocuPanda - Document Understanding

Creates standardizations in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/standardize/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Standardize Documents](https://docs.docupipe.ai/openapi/docupanda.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to be standardized, up to 100 per batch. |
| `forceRecompute` | body | `boolean` | no | Whether to recompute standardizations for documents that have already been standardized. |
| `guidelines` | body | `string` | no | Guidelines to apply to the schema when standardizing. If this is provided, it will override the schema guidelines. |
| `schemaId` | body | `string` | yes | Unique identifier of the schema to be used for standardization. |
| `standardizationMode` | body | `object` | no | — |
