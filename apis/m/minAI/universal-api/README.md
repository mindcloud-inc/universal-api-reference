# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-1min-ai-48x48_1776886329110.png" alt="1minAI logo" width="28" height="28"> 1minAI: Universal API

Generate AI text, images, audio, video, captions, and code with 1minAI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/minAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://1min.ai
- **Vendor API docs:** https://docs.1min.ai/docs/api/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Chat with AI](actions/chat-with-ai.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/chat-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "Explain quantum computing in simple terms"
}'
```

## Actions (24)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Upload asset](actions/upload-asset.md) | POST | Uploads an asset file to 1minAI. |

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Convert text to speech](actions/convert-text-to-speech.md) | POST | Creates speech audio from text in 1minAI. |

### Captions

| Action | Method | Description |
| --- | --- | --- |
| [Generate captions](actions/generate-captions.md) | POST | Creates captions and transcripts for video in 1minAI. |

### Chat Response

| Action | Method | Description |
| --- | --- | --- |
| [Chat with AI](actions/chat-with-ai.md) | POST | Creates an AI chat response in 1minAI. |

### Code

| Action | Method | Description |
| --- | --- | --- |
| [Generate code](actions/generate-code.md) | POST | Creates code from a prompt in 1minAI. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create conversation](actions/create-conversation.md) | POST | Creates a new conversation in 1minAI. |

### Generated Content

| Action | Method | Description |
| --- | --- | --- |
| [Check grammar](actions/check-grammar.md) | POST | Checks and corrects text grammar in 1minAI. |
| [Expand content](actions/expand-content.md) | POST | Creates expanded text content in 1minAI. |
| [Generate advertisements](actions/generate-advertisements.md) | POST | Creates advertisement copy drafts in 1minAI. |
| [Generate blog article](actions/generate-blog-article.md) | POST | Creates a blog article in 1minAI. |
| [Generate brand voice content](actions/generate-brand-voice-content.md) | POST | Creates brand voice content in 1minAI. |
| [Generate comments](actions/generate-comments.md) | POST | Creates social media comments in 1minAI. |
| [Generate emails](actions/generate-emails.md) | POST | Creates email message drafts in 1minAI. |
| [Generate social media posts](actions/generate-social-media-posts.md) | POST | Creates social media posts in 1minAI. |
| [Paraphrase content](actions/paraphrase-content.md) | POST | Creates paraphrased text content in 1minAI. |
| [Rewrite content](actions/rewrite-content.md) | POST | Creates rewritten text content in 1minAI. |
| [Shorten content](actions/shorten-content.md) | POST | Creates shortened text content in 1minAI. |
| [Summarize content](actions/summarize-content.md) | POST | Creates bullet-point content summaries in 1minAI. |
| [Translate content](actions/translate-content.md) | POST | Creates translated text content in 1minAI. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create image variations](actions/create-image-variations.md) | POST | Creates image variations from an uploaded image in 1minAI. |
| [Generate image](actions/generate-image.md) | POST | Creates an image from a text prompt in 1minAI. |

### Keyword Research

| Action | Method | Description |
| --- | --- | --- |
| [Research keywords](actions/keyword-research.md) | POST | Finds keyword ideas and metrics in 1minAI. |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Generate image prompt](actions/generate-image-prompt.md) | POST | Creates text prompts from uploaded images in 1minAI. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate text to video](actions/generate-text-to-video.md) | POST | Creates a video from text in 1minAI. |

