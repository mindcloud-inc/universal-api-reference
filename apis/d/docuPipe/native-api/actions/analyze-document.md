# Analyze Document with DocuPipe

Analyzes a document in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/analyze/document`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Analyze Document](https://docs.docupipe.ai/reference/post_analyze_document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | yes | Unique identifier of the document to be questioned. |
| `questions[]` | body | `array<string>` | yes | List of questions to be answered. |
| `instructions` | body | `string` | no | Global instructions to provide additional guidelines or context to the AI when answering the questions. |
| `pages[]` | body | `array<number>` | no | List of page numbers to be analyzed (zero indexed). If not provided, all pages will be analyzed. |
