# Classify Documents with DocuPipe

Classifies documents in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/classify/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Classify Documents](https://docs.docupipe.ai/reference/post_classify_batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds[]` | body | `array<string>` | yes | List of document IDs to classify |
| `classIds[]` | body | `array<string>` | no | List of class IDs to use for classification |
| `multiClass` | body | `boolean` | no | Whether to allow multiple classifications per document |
| `includeUnknown` | body | `boolean` | no | Whether to include the 'unknown' class in the classification (only relevant if multiClass is false) |
| `instructions` | body | `string` | no | Instructions for the AI on how to classify the documents |
| `displayMode` | body | `list` | no | *Advanced Feature* Mode of display to run. The options are: `auto`: AI decides how to display the document (default) `spatial`: Display text spatially, as it appears in the document `sections`: Display text from top to bottom as sections, with tables appearing as markdown `image`: Display as an image. Accepted values: `auto`, `image`, `sections`, `spatial`. |
