# <img src="https://images.mindcloud.co/apps/icons/de-api_1776088101079.png" alt="deAPI logo" width="28" height="28"> deAPI: Universal API

Run image, video, audio, OCR, transcription, embeddings, and other open-source AI workloads through deAPI's unified inference API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deAPI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://deapi.ai/
- **Vendor API docs:** https://docs.deapi.ai/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Balance](actions/get-current-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-current-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Audio Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Text-to-Speech Job](actions/create-text-to-speech-job.md) | POST | Creates a text-to-speech job in deAPI. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Balance](actions/get-current-balance.md) | GET | Retrieves your current account balance from deAPI. |

### Embedding Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Text-to-Embedding Job](actions/create-text-to-embedding-job.md) | POST | Creates a text-to-embedding job in deAPI. |

### Image Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Text-to-Image Job](actions/create-text-to-image-job.md) | POST | Creates a text-to-image job in deAPI. |

### Image Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Enhance Image Prompt](actions/enhance-image-prompt.md) | GET | Enhances a text-to-image prompt in deAPI. |

### Image Prompt Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Image Prompt Price](actions/calculate-image-prompt-price.md) | GET | Calculates image prompt enhancement pricing in deAPI. |

### Job Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Request Status](actions/get-request-status.md) | GET | Retrieves the status of an inference job from deAPI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available inference models from deAPI. |

### Music Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Text-to-Music Job](actions/create-text-to-music-job.md) | POST | Creates a text-to-music job in deAPI. |

### Sample Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Get Sample Prompts](actions/get-sample-prompts.md) | GET | Retrieves sample prompts for AI tasks from deAPI. |

### Speech Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Enhance Speech Prompt](actions/enhance-speech-prompt.md) | GET | Enhances a text-to-speech prompt in deAPI. |

### Text-to-embedding Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Text-to-Embedding Price](actions/calculate-text-to-embedding-price.md) | GET | Calculates text-to-embedding request pricing in deAPI. |

### Text-to-image Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Text-to-Image Price](actions/calculate-text-to-image-price.md) | GET | Calculates text-to-image request pricing in deAPI. |

### Text-to-music Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Text-to-Music Price](actions/calculate-text-to-music-price.md) | GET | Calculates text-to-music request pricing in deAPI. |

### Text-to-speech Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Text-to-Speech Price](actions/calculate-text-to-speech-price.md) | GET | Calculates text-to-speech request pricing in deAPI. |

### Text-to-video Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Text-to-Video Price](actions/calculate-text-to-video-price.md) | GET | Calculates text-to-video request pricing in deAPI. |

### Transcription Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Transcription Job](actions/create-transcription-job.md) | POST |  |

### Transcription Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Video Transcription Price](actions/calculate-transcription-price.md) | GET |  |

### Video Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Text-to-Video Job](actions/create-text-to-video-job.md) | POST | Creates a text-to-video job in deAPI. |

