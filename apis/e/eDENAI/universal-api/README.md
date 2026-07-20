# <img src="https://images.mindcloud.co/apps/icons/e-denai_1774643101551.png" alt="EDEN AI logo" width="28" height="28"> EDEN AI: Universal API

Access Eden AI's unified V3 API for text, OCR, image, translation, audio, video, and LLM workflows through one integration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eDENAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.edenai.co
- **Vendor API docs:** https://docs.edenai.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Async Job

| Action | Method | Description |
| --- | --- | --- |
| [List Async Jobs](actions/list-async-jobs.md) | GET | Retrieves asynchronous jobs from EDEN AI. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your available credits from EDEN AI. |

### Feature Catalog

| Action | Method | Description |
| --- | --- | --- |
| [List Features](actions/list-features.md) | GET | Retrieves available features from EDEN AI. |

### Feature Category

| Action | Method | Description |
| --- | --- | --- |
| [List Audio Subfeatures](actions/list-audio-subfeatures.md) | GET | Retrieves available audio subfeatures from EDEN AI. |
| [List Image Subfeatures](actions/list-image-subfeatures.md) | GET | Retrieves available image subfeatures from EDEN AI. |
| [List OCR Subfeatures](actions/list-ocr-subfeatures.md) | GET | Retrieves available OCR subfeatures from EDEN AI. |
| [List Text Subfeatures](actions/list-text-subfeatures.md) | GET | Retrieves available text subfeatures from EDEN AI. |
| [List Translation Subfeatures](actions/list-translation-subfeatures.md) | GET | Retrieves available translation subfeatures from EDEN AI. |
| [List Video Subfeatures](actions/list-video-subfeatures.md) | GET | Retrieves available video subfeatures from EDEN AI. |

### Feature Detail

| Action | Method | Description |
| --- | --- | --- |
| [Get Background Removal Info](actions/get-background-removal-info.md) | GET | Retrieves feature information for background removal in EDEN AI. |
| [Get Deepfake Detection Info](actions/get-deepfake-detection-info.md) | GET | Retrieves feature information for deepfake detection in EDEN AI. |
| [Get Document Translation Info](actions/get-document-translation-info.md) | GET | Retrieves feature information for document translation in EDEN AI. |
| [Get Explicit Content Info](actions/get-explicit-content-info.md) | GET | Retrieves feature information for explicit content in EDEN AI. |
| [Get Face Compare Info](actions/get-face-compare-info.md) | GET | Retrieves feature information for face comparison in EDEN AI. |
| [Get Face Detection Info](actions/get-face-detection-info.md) | GET | Retrieves feature information for face detection in EDEN AI. |
| [Get Financial Parser Info](actions/get-financial-parser-info.md) | GET | Retrieves feature information for financial parsing in EDEN AI. |
| [Get Identity Parser Info](actions/get-identity-parser-info.md) | GET | Retrieves feature information for identity parsing in EDEN AI. |
| [Get Image AI Detection Info](actions/get-image-ai-detection-info.md) | GET | Retrieves feature information for image AI detection in EDEN AI. |
| [Get Image Anonymization Info](actions/get-image-anonymization-info.md) | GET | Retrieves feature information for image anonymization in EDEN AI. |
| [Get Image Generation Info](actions/get-image-generation-info.md) | GET | Retrieves feature information for image generation in EDEN AI. |
| [Get Logo Detection Info](actions/get-logo-detection-info.md) | GET | Retrieves feature information for logo detection in EDEN AI. |
| [Get Named Entity Recognition Info](actions/get-named-entity-recognition-info.md) | GET | Retrieves feature information for named entity recognition in EDEN AI. |
| [Get Object Detection Info](actions/get-object-detection-info.md) | GET | Retrieves feature information for object detection in EDEN AI. |
| [Get OCR Info](actions/get-ocr-info.md) | GET | Retrieves feature information for OCR in EDEN AI. |
| [Get OCR Multipage Info](actions/get-ocr-multipage-info.md) | GET | Retrieves feature information for multipage OCR in EDEN AI. |
| [Get OCR Tables Info](actions/get-ocr-tables-info.md) | GET | Retrieves feature information for OCR tables in EDEN AI. |
| [Get Plagiarism Detection Info](actions/get-plagiarism-detection-info.md) | GET | Retrieves feature information for plagiarism detection in EDEN AI. |
| [Get Resume Parser Info](actions/get-resume-parser-info.md) | GET | Retrieves feature information for resume parsing in EDEN AI. |
| [Get Speech To Text Info](actions/get-speech-to-text-info.md) | GET | Retrieves feature information for speech-to-text in EDEN AI. |
| [Get Spell Check Info](actions/get-spell-check-info.md) | GET | Retrieves feature information for spell check in EDEN AI. |
| [Get Text AI Detection Info](actions/get-text-ai-detection-info.md) | GET | Retrieves feature information for text AI detection in EDEN AI. |
| [Get Text Moderation Info](actions/get-text-moderation-info.md) | GET | Retrieves feature information for text moderation in EDEN AI. |
| [Get Text To Speech Info](actions/get-text-to-speech-info.md) | GET | Retrieves feature information for text-to-speech in EDEN AI. |
| [Get Topic Extraction Info](actions/get-topic-extraction-info.md) | GET | Retrieves feature information for topic extraction in EDEN AI. |
| [Get Translation Info](actions/get-translation-info.md) | GET | Retrieves feature information for translation in EDEN AI. |
| [Get Video Generation Info](actions/get-video-generation-info.md) | GET | Retrieves feature information for video generation in EDEN AI. |

### Moderation Result

| Action | Method | Description |
| --- | --- | --- |
| [Moderate Text](actions/moderate-text.md) | POST | Creates a text moderation request in EDEN AI. |

