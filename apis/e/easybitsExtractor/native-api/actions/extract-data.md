# Extract Data with easybits Extractor

Extracts structured data from documents in easybits Extractor.

## Endpoint

- **Method:** `POST`
- **Path:** `/pipelines/:pipelineId`
- **Base URL:** `https://extractor.easybits.tech/api`
- **Official documentation:** [Extract Data](https://extractor.easybits.tech/documentation/integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<string>` | yes | One or more document URLs or base64 data URLs to extract. |
