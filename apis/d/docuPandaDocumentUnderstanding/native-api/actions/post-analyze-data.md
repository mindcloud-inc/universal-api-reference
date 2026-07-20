# Analyze Data with DocuPanda - Document Understanding

Creates a batch analysis in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/analyze/data`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Analyze Data](https://docs.docupipe.ai/reference/post_analyze_data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | no | Dataset which defines what documents are included in the analysis. If both dataset and documentIds are provided, we take the intersection of the two. |
| `documentIds` | body | `list<string>` | no | List of document IDs to analyze. If both dataset and documentIds are provided, we take the intersection of the two. |
| `instructions` | body | `string` | no | Global instructions to provide additional guidelines or context to the AI when answering the questions. |
| `questions` | body | `list<string>` | yes | List of questions to be answered. |
| `schemaId` | body | `string` | no | Unique identifier of the schema to be used for the analysis. If provided, only those documents with a valid standardization under this schema will be included in the analysis. |
