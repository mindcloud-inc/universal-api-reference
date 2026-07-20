# Standardize V2 (Stable) with DocuPipe

Standardizes documents in DocuPipe using V2.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/standardize/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Standardize V2 (Stable)](https://docs.docupipe.ai/reference/post_standardize_batch_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to be standardized, up to 100 per batch. |
| `schemaId` | body | `string` | no | Unique identifier of the schema to be used for standardization - if not provided, one will be inferred. |
| `guidelines` | body | `string` | no | Guidelines to apply to the schema when standardizing. If this is provided, it will override the schema guidelines. |
| `useMetadata` | body | `boolean` | no | Whether to use metadata during standardization. |
| `displayMode` | body | `list` | no | *Advanced Feature* Mode of display to run. The options are: `auto`: AI decides how to display the document (default) `spatial`: Display text spatially, as it appears in the document `sections`: Display text from top to bottom as sections, with tables appearing as markdown `image`: Display as an image, accompanied by section view Accepted values: `auto`, `image`, `sections`, `spatial`. |
| `splitMode` | body | `list` | no | *Advanced Feature* Mode of splitting to run. Splitting is used to extract array fields efficiently. The options are: `auto`: AI decides how to split the document (default) `never`: Never split the document (this could lead to errors or poor performance for large documents) `all`: Split the document into individual pages Accepted values: `all`, `auto`, `never`. |
| `effortLevel` | body | `list` | no | *Advanced Feature* Level of effort to run. The options are: `standard`: Standard effort level (default) `high`: High effort level, for more difficult documents Accepted values: `extended`, `high`, `standard`. |
| `stdVersion` | body | `list` | no | Version of the standardization job. Options: 2.0, 2.1, 2.2 (default, stable), 2.3 (experimental, higher quality but may have runtime instability). Accepted values: `2`, `2.1`, `2.2`, `2.3`. |
| `pages[]` | body | `array<array>` | no | *Advanced Feature* For every document, list of all pages that you want want to standardize.  Page numbers are zero-indexed positions within each uploaded document. If not provided, the entire document will be standardized. |
| `timeout` | body | `number` | no | The job timeout (in seconds) for webhook error reporting |
