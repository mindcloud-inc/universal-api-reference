# JigsawStack: Native API Reference

A consolidated summary of JigsawStack's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://jigsawstack.com/docs/api-reference/all-models
- **API base URL:** `https://api.jigsawstack.com`

## Authentication

### API Key

Use a JigsawStack secret key for backend access. Secret keys can access all documented APIs.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://jigsawstack.com/docs/api-reference/authentication)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Sentiment](actions/analyze-sentiment.md) | `POST /v1/ai/sentiment` | [docs](https://jigsawstack.com/docs/api-reference/ai/sentiment) |
| [Classify Dataset](actions/classify-dataset.md) | `POST /v1/classification` | [docs](https://jigsawstack.com/docs/api-reference/classification/classification) |
| [Convert HTML to Target Format](actions/convert-html-to-target-format.md) | `POST /v1/web/html_to_any` | [docs](https://jigsawstack.com/docs/api-reference/web/html-to-any) |
| [Convert Text to SQL](actions/convert-text-to-sql.md) | `POST /v1/ai/sql` | [docs](https://jigsawstack.com/docs/api-reference/ai/text-to-sql) |
| [Create Prompt](actions/create-prompt.md) | `POST /v1/prompt_engine` | [docs](https://jigsawstack.com/docs/api-reference/prompt-engine/create) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/store/file/read/{key}` | [docs](https://jigsawstack.com/docs/api-reference/store/file/delete) |
| [Delete Prompt](actions/delete-prompt.md) | `DELETE /v1/prompt_engine/{id}` | [docs](https://jigsawstack.com/docs/api-reference/prompt-engine/delete) |
| [Detect NSFW Content](actions/detect-nsfw-content.md) | `POST /v1/validate/nsfw` | [docs](https://jigsawstack.com/docs/api-reference/validate/nsfw) |
| [Detect Objects](actions/detect-objects.md) | `POST /v1/object_detection` | [docs](https://jigsawstack.com/docs/api-reference/ai/object-detection) |
| [Detect Profanity](actions/detect-profanity.md) | `POST /v1/validate/profanity` | [docs](https://jigsawstack.com/docs/api-reference/validate/profanity) |
| [Detect Spam](actions/detect-spam.md) | `POST /v1/validate/spam_check` | [docs](https://jigsawstack.com/docs/api-reference/validate/spam-check) |
| [Detect Spelling Errors](actions/detect-spelling-errors.md) | `POST /v1/validate/spell_check` | [docs](https://jigsawstack.com/docs/api-reference/validate/spell-check) |
| [Extract Text with vOCR](actions/extract-text-with-vocr.md) | `POST /v1/vocr` | [docs](https://jigsawstack.com/docs/api-reference/ai/vocr) |
| [Generate Embedding](actions/generate-embedding.md) | `POST /v1/embedding` | [docs](https://jigsawstack.com/docs/api-reference/ai/embedding) |
| [Generate Embedding v2](actions/generate-embedding-v2.md) | `POST /v2/embedding` | [docs](https://jigsawstack.com/docs/api-reference/ai/embedding-v2) |
| [Generate Image](actions/generate-image.md) | `POST /v1/ai/image_generation` | [docs](https://jigsawstack.com/docs/api-reference/ai/image-generation) |
| [Get Prompt](actions/get-prompt.md) | `GET /v1/prompt_engine/{id}` | [docs](https://jigsawstack.com/docs/api-reference/prompt-engine/retrieve) |
| [Get Search Suggestions](actions/get-search-suggestions.md) | `GET /v1/web/search/suggest` | [docs](https://jigsawstack.com/docs/api-reference/web/search-suggestions) |
| [List Prompts](actions/list-prompts.md) | `GET /v1/prompt_engine` | [docs](https://jigsawstack.com/docs/api-reference/prompt-engine/list) |
| [Predict Time Series](actions/predict-time-series.md) | `POST /v1/ai/prediction` | [docs](https://jigsawstack.com/docs/api-reference/ai/prediction) |
| [Retrieve File](actions/retrieve-file.md) | `GET /v1/store/file/read/{key}` | [docs](https://jigsawstack.com/docs/api-reference/store/file/get) |
| [Run Deep Research](actions/run-deep-research.md) | `POST /v1/web/deep_research` | [docs](https://jigsawstack.com/docs/api-reference/web/deep-research) |
| [Run Prompt Direct](actions/run-prompt-direct.md) | `POST /v1/prompt_engine/run` | [docs](https://jigsawstack.com/docs/api-reference/prompt-engine/run-direct) |
| [Run Saved Prompt](actions/run-saved-prompt.md) | `POST /v1/prompt_engine/{id}` | [docs](https://jigsawstack.com/docs/api-reference/prompt-engine/run) |
| [Scrape Web Page with AI](actions/scrape-web-page-with-ai.md) | `POST /v1/ai/scrape` | [docs](https://jigsawstack.com/docs/api-reference/ai/scrape) |
| [Search the Web](actions/search-the-web.md) | `POST /v1/web/search` | [docs](https://jigsawstack.com/docs/api-reference/web/ai-search) |
| [Summarize Text](actions/summarize-text.md) | `POST /v1/ai/summary` | [docs](https://jigsawstack.com/docs/api-reference/ai/summary) |
| [Transcribe Audio](actions/transcribe-audio.md) | `POST /v1/ai/transcribe` | [docs](https://jigsawstack.com/docs/api-reference/ai/speech-to-text) |
| [Translate Image Text](actions/translate-image-text.md) | `POST /v1/ai/translate/image` | [docs](https://jigsawstack.com/docs/api-reference/ai/translate/image-translate) |
| [Translate Text](actions/translate-text.md) | `POST /v1/ai/translate` | [docs](https://jigsawstack.com/docs/api-reference/ai/translate/translate) |
| [Upload File](actions/upload-file.md) | `POST /v1/store/file` | [docs](https://jigsawstack.com/docs/api-reference/store/file/add) |
