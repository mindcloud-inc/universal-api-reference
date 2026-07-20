# 1minAI: Native API Reference

A consolidated summary of 1minAI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.1min.ai/docs/api/intro
- **API base URL:** `https://api.1min.ai`

## Authentication

### API Key

Use your 1minAI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.1min.ai/docs/api/create-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chat with AI](actions/chat-with-ai.md) | `POST /api/chat-with-ai` | [docs](https://docs.1min.ai/docs/api/chat-with-ai-api) |
| [Check grammar](actions/check-grammar.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/grammar-checker/grammar-checker-tag) |
| [Convert text to speech](actions/convert-text-to-speech.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-audio/text-to-speech/openai) |
| [Create conversation](actions/create-conversation.md) | `POST /api/conversations` | [docs](https://docs.1min.ai/docs/api/chat-with-ai-api) |
| [Create image variations](actions/create-image-variations.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-image/image-variator/flux-redux-schnell-image-variator) |
| [Expand content](actions/expand-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-expander/content-expander-tag) |
| [Generate advertisements](actions/generate-advertisements.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-advertisements) |
| [Generate blog article](actions/generate-blog-article.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-blog-article) |
| [Generate brand voice content](actions/generate-brand-voice-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-brand-voice) |
| [Generate captions](actions/generate-captions.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-video/caption-generator/caption-generator-tag) |
| [Generate code](actions/generate-code.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-code/code-generator/code-generator-tag) |
| [Generate comments](actions/generate-comments.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-comments) |
| [Generate emails](actions/generate-emails.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-emails) |
| [Generate image](actions/generate-image.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-image/image-generator/gpt-image-1-mini-image-generation) |
| [Generate image prompt](actions/generate-image-prompt.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-image/image-to-prompt/image-to-prompt-tag) |
| [Generate social media posts](actions/generate-social-media-posts.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-generator/content-generator-social-media-posts) |
| [Generate text to video](actions/generate-text-to-video.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-video/text-to-video/sora-text-to-video) |
| [Research keywords](actions/keyword-research.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/keyword-research/keyword-research-tag) |
| [Paraphrase content](actions/paraphrase-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-paraphraser/content-paraphraser-tag) |
| [Rewrite content](actions/rewrite-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/rewriter/rewriter-tag) |
| [Shorten content](actions/shorten-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-shortener/content-shortener-tag) |
| [Summarize content](actions/summarize-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-summarizer/content-summarizer-tag) |
| [Translate content](actions/translate-content.md) | `POST /api/features` | [docs](https://docs.1min.ai/docs/api/ai-for-writing/content-translator/content-translator-tag) |
| [Upload asset](actions/upload-asset.md) | `POST /api/assets` | [docs](https://docs.1min.ai/docs/api/asset-api) |
