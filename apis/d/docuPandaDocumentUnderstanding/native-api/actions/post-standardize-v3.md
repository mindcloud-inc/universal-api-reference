# Standardize V3 (Beta) with DocuPanda - Document Understanding

Creates V3 standardizations in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/standardize`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Standardize V3 (Beta)](https://docs.docupipe.ai/reference/post_standardize_v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | yes | Unique identifier of the document to be standardized. |
| `pages` | body | `list<number>` | no | Optional list of 0-indexed page numbers to standardize. If not provided, the entire document will be standardized. |
| `schemaId` | body | `string` | yes | Schema to use for standardization (required for V3). |
| `guidelines` | body | `string` | no | Extraction guidelines. Overrides schema guidelines. |
| `useMetadata` | body | `boolean` | no | Whether to use metadata during standardization. |
| `pages[]` | body | `array<number>` | no | Optional list of 0-indexed page numbers to standardize. If not provided, the entire document will be standardized. |
| `stdVersion` | body | `number` | no | — |
| `effortLevel` | body | `string` | no | — |
| `timeout` | body | `number` | no | The job timeout (in seconds) for webhook error reporting |
