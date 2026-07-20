# Analyze Data with DocuPipe

Analyzes structured data in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/analyze/data`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Analyze Data](https://docs.docupipe.ai/reference/post_analyze_data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | no | List of document IDs to analyze. If both dataset and documentIds are provided, we take the intersection of the two. |
| `dataset` | body | `string` | no | Dataset which defines what documents are included in the analysis. If both dataset and documentIds are provided, we take the intersection of the two. |
| `schemaId` | body | `string` | no | Unique identifier of the schema to be used for the analysis. If provided, only those documents with a valid standardization under this schema will be included in the analysis. |
| `questions[]` | body | `array<string>` | yes | List of questions to be answered. |
| `instructions` | body | `string` | no | Global instructions to provide additional guidelines or context to the AI when answering the questions. |
