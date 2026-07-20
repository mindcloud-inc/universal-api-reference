# EDEN AI: Native API Reference

A consolidated summary of EDEN AI's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.edenai.co
- **REST API base URL:** `https://api.edenai.run/v3`
- **REST API base URL:** `https://api.edenai.run/v2`

## Authentication

### API Key

Implicit Eden AI bearer token authentication using the platform-managed apiKey credential path.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.edenai.co/v3/get-started/introduction)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

- **REST API:** Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

- **REST API:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Background Removal Info](actions/get-background-removal-info.md) | `GET /info/image/background_removal` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Credits](actions/get-credits.md) | `GET https://api.edenai.run/v2/cost_management/credits/` | [docs](https://docs.edenai.co/api-reference/cost-monitoring/my-credits) |
| [Get Deepfake Detection Info](actions/get-deepfake-detection-info.md) | `GET /info/image/deepfake_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Document Translation Info](actions/get-document-translation-info.md) | `GET /info/translation/document_translation` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Explicit Content Info](actions/get-explicit-content-info.md) | `GET /info/image/explicit_content` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Face Compare Info](actions/get-face-compare-info.md) | `GET /info/image/face_compare` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Face Detection Info](actions/get-face-detection-info.md) | `GET /info/image/face_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Financial Parser Info](actions/get-financial-parser-info.md) | `GET /info/ocr/financial_parser` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Identity Parser Info](actions/get-identity-parser-info.md) | `GET /info/ocr/identity_parser` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Image AI Detection Info](actions/get-image-ai-detection-info.md) | `GET /info/image/ai_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Image Anonymization Info](actions/get-image-anonymization-info.md) | `GET /info/image/anonymization` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Image Generation Info](actions/get-image-generation-info.md) | `GET /info/image/generation` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Logo Detection Info](actions/get-logo-detection-info.md) | `GET /info/image/logo_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Named Entity Recognition Info](actions/get-named-entity-recognition-info.md) | `GET /info/text/named_entity_recognition` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Object Detection Info](actions/get-object-detection-info.md) | `GET /info/image/object_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get OCR Info](actions/get-ocr-info.md) | `GET /info/ocr/ocr` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get OCR Multipage Info](actions/get-ocr-multipage-info.md) | `GET /info/ocr/ocr_async` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get OCR Tables Info](actions/get-ocr-tables-info.md) | `GET /info/ocr/ocr_tables_async` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Plagiarism Detection Info](actions/get-plagiarism-detection-info.md) | `GET /info/text/plagia_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Resume Parser Info](actions/get-resume-parser-info.md) | `GET /info/ocr/resume_parser` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Speech To Text Info](actions/get-speech-to-text-info.md) | `GET /info/audio/speech_to_text_async` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Spell Check Info](actions/get-spell-check-info.md) | `GET /info/text/spell_check` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Text AI Detection Info](actions/get-text-ai-detection-info.md) | `GET /info/text/ai_detection` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Text Moderation Info](actions/get-text-moderation-info.md) | `GET /info/text/moderation` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Text To Speech Info](actions/get-text-to-speech-info.md) | `GET /info/audio/tts` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Topic Extraction Info](actions/get-topic-extraction-info.md) | `GET /info/text/topic_extraction` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Translation Info](actions/get-translation-info.md) | `GET /info/translation/automatic_translation` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [Get Video Generation Info](actions/get-video-generation-info.md) | `GET /info/video/generation_async` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/get-feature-info) |
| [List Async Jobs](actions/list-async-jobs.md) | `GET /universal-ai/async` | [docs](https://docs.edenai.co/api-reference/universal-ai/list-async-jobs) |
| [List Audio Subfeatures](actions/list-audio-subfeatures.md) | `GET /info/audio` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-subfeatures) |
| [List Features](actions/list-features.md) | `GET /info` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-features) |
| [List Image Subfeatures](actions/list-image-subfeatures.md) | `GET /info/image` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-subfeatures) |
| [List OCR Subfeatures](actions/list-ocr-subfeatures.md) | `GET /info/ocr` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-subfeatures) |
| [List Text Subfeatures](actions/list-text-subfeatures.md) | `GET /info/text` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-subfeatures) |
| [List Translation Subfeatures](actions/list-translation-subfeatures.md) | `GET /info/translation` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-subfeatures) |
| [List Video Subfeatures](actions/list-video-subfeatures.md) | `GET /info/video` | [docs](https://docs.edenai.co/api-reference/universal-ai-info/list-subfeatures) |
| [Moderate Text](actions/moderate-text.md) | `POST /universal-ai` | [docs](https://docs.edenai.co/api-reference/universal-ai/universal-ai) |
