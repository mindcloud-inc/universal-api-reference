# <img src="https://images.mindcloud.co/apps/icons/images_1775056519969.jpeg" alt="JigsawStack logo" width="28" height="28"> JigsawStack: Universal API

Generate, search, scrape, and analyze multimodal content with AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jigsawStack/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jigsawstack.com
- **Vendor API docs:** https://jigsawstack.com/docs/api-reference/all-models

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Search Suggestions](actions/get-search-suggestions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/get-search-suggestions?connectionId=$CONNECTION_ID&query=What%20is%20the%20capital" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify Dataset](actions/classify-dataset.md) | GET |  |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Generate Embedding](actions/generate-embedding.md) | GET |  |
| [Generate Embedding v2](actions/generate-embedding-v2.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Retrieve File](actions/retrieve-file.md) | GET |  |
| [Upload File](actions/upload-file.md) | POST |  |

### Html Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert HTML to Target Format](actions/convert-html-to-target-format.md) | GET |  |

### Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | GET |  |

### Image Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate Image Text](actions/translate-image-text.md) | GET |  |

### Nsfw Validation

| Action | Method | Description |
| --- | --- | --- |
| [Detect NSFW Content](actions/detect-nsfw-content.md) | GET |  |

### Object Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Objects](actions/detect-objects.md) | GET |  |

### Ocr

| Action | Method | Description |
| --- | --- | --- |
| [Extract Text with vOCR](actions/extract-text-with-vocr.md) | GET |  |

### Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Predict Time Series](actions/predict-time-series.md) | GET |  |

### Profanity Validation

| Action | Method | Description |
| --- | --- | --- |
| [Detect Profanity](actions/detect-profanity.md) | GET |  |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST |  |
| [Delete Prompt](actions/delete-prompt.md) | DELETE |  |
| [Get Prompt](actions/get-prompt.md) | GET |  |
| [List Prompts](actions/list-prompts.md) | GET |  |
| [Run Prompt Direct](actions/run-prompt-direct.md) | GET |  |
| [Run Saved Prompt](actions/run-saved-prompt.md) | GET |  |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Suggestions](actions/get-search-suggestions.md) | GET |  |
| [Run Deep Research](actions/run-deep-research.md) | GET |  |
| [Search the Web](actions/search-the-web.md) | GET |  |

### Sentiment Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Sentiment](actions/analyze-sentiment.md) | GET |  |

### Spam Validation

| Action | Method | Description |
| --- | --- | --- |
| [Detect Spam](actions/detect-spam.md) | GET |  |

### Spell Check

| Action | Method | Description |
| --- | --- | --- |
| [Detect Spelling Errors](actions/detect-spelling-errors.md) | GET |  |

### Sql Query

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text to SQL](actions/convert-text-to-sql.md) | GET |  |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Text](actions/summarize-text.md) | GET |  |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Transcribe Audio](actions/transcribe-audio.md) | GET |  |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate Text](actions/translate-text.md) | GET |  |

### Web Scrape

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Web Page with AI](actions/scrape-web-page-with-ai.md) | GET |  |

