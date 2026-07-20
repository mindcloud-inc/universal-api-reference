# Standardize V2 (Stable) with DocuPanda - Document Understanding

Creates V2 standardizations in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/standardize/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Standardize V2 (Stable)](https://docs.docupipe.ai/reference/post_standardize_batch_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to be standardized, up to 100 per batch. |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to be standardized, up to 100 per batch. |
| `pages` | body | `list<object>` | no | *Advanced Feature* For every document, list of all pages that you want want to standardize.  Page numbers are zero-indexed positions within each uploaded document. If not provided, the entire document will be standardized. |
| `schemaId` | body | `string` | no | Unique identifier of the schema to be used for standardization - if not provided, one will be inferred. |
| `guidelines` | body | `string` | no | Guidelines to apply to the schema when standardizing. If this is provided, it will override the schema guidelines. |
| `useMetadata` | body | `boolean` | no | Whether to use metadata during standardization. |
| `displayMode` | body | `string` | no | — |
| `splitMode` | body | `string` | no | — |
| `effortLevel` | body | `string` | no | — |
| `stdVersion` | body | `number` | no | — |
| `pages[]` | body | `array<string>` | no | *Advanced Feature* For every document, list of all pages that you want want to standardize.  Page numbers are zero-indexed positions within each uploaded document. If not provided, the entire document will be standardized. |
| `timeout` | body | `number` | no | The job timeout (in seconds) for webhook error reporting |
