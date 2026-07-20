# Classify Documents with DocuPanda - Document Understanding

Creates document classifications in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/classify/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Classify Documents](https://docs.docupipe.ai/reference/post_classify_batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classIds` | body | `list<string>` | no | List of class IDs to use for classification |
| `displayMode` | body | `string` | no | — |
| `documentIds` | body | `list<string>` | yes | List of document IDs to classify |
| `includeUnknown` | body | `boolean` | no | Whether to include the 'unknown' class in the classification (only relevant if multiClass is false) |
| `instructions` | body | `string` | no | Instructions for the AI on how to classify the documents |
| `multiClass` | body | `boolean` | no | Whether to allow multiple classifications per document |
