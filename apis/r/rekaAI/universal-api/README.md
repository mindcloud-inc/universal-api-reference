# <img src="https://images.mindcloud.co/apps/icons/reka-ai-icon-square_1775851267464.png" alt="Reka AI logo" width="28" height="28"> Reka AI: Universal API

Reka AI provides multimodal APIs for chat completions, research agents, speech, image workflows, video intelligence, clip generation, and metadata extraction.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rekaAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reka.ai
- **Vendor API docs:** https://docs.reka.ai/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Reel](actions/create-reel.md) | POST | Creates a reel in Reka AI. |
| [Delete Image](actions/delete-image.md) | DELETE | Deletes an existing image from Reka AI. |
| [Delete Legacy Video](actions/delete-legacy-video.md) | DELETE | Deletes an existing legacy video from Reka AI. |
| [Delete Reel](actions/delete-reel.md) | DELETE | Deletes an existing reel from Reka AI. |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes an existing video from Reka AI. |
| [Get Image](actions/get-image.md) | GET | Retrieves an image from Reka AI. |
| [Get Images](actions/get-images.md) | GET | Retrieves images from Reka AI. |
| [Get Legacy Video](actions/get-legacy-video.md) | GET | Retrieves a legacy video from Reka AI. |
| [Get Reel](actions/get-reel.md) | GET | Retrieves a reel from Reka AI. |
| [Get Video](actions/get-video.md) | GET | Retrieves a video from Reka AI. |
| [List Group Videos](actions/list-group-videos.md) | GET | Retrieves videos from a Reka AI video group. |
| [List Legacy Group Videos](actions/list-legacy-group-videos.md) | GET | Retrieves videos from a Reka AI legacy video group. |
| [List Legacy Videos](actions/list-legacy-videos.md) | GET | Retrieves legacy videos from Reka AI. |
| [List Reels](actions/list-reels.md) | GET | Retrieves reels from Reka AI. |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from Reka AI. |
| [Search Images](actions/search-images.md) | GET | Finds images in Reka AI by query. |
| [Search Videos](actions/search-videos.md) | GET | Finds videos in Reka AI by query. |
| [Update Video Metadata](actions/update-video-metadata.md) | PUT | Updates video metadata in Reka AI. |
| [Upload Images](actions/upload-images.md) | POST | Uploads images to Reka AI. |
| [Upload Legacy Video](actions/upload-legacy-video.md) | POST | Uploads a legacy video to Reka AI. |
| [Upload Video](actions/upload-video.md) | POST | Uploads a video to Reka AI. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Reka AI. |
| [Create Research Chat Completion](actions/create-research-chat-completion.md) | POST | Creates a research chat completion in Reka AI. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Ask Video QA](actions/ask-video-qa.md) | POST | Creates a video QA response in Reka AI. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Group](actions/create-video-group.md) | POST | Creates a video group in Reka AI. |
| [List Video Groups](actions/list-video-groups.md) | GET | Retrieves video groups from Reka AI. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Legacy Video Group](actions/create-legacy-video-group.md) | POST | Creates a legacy video group in Reka AI. |
| [Delete Legacy Video Group](actions/delete-legacy-video-group.md) | DELETE | Deletes an existing legacy video group from Reka AI. |
| [Delete Video Group](actions/delete-video-group.md) | DELETE | Deletes an existing video group from Reka AI. |
| [Get Legacy Video Group](actions/get-legacy-video-group.md) | GET | Retrieves a legacy video group from Reka AI. |
| [Get Video Group](actions/get-video-group.md) | GET | Retrieves a video group from Reka AI. |
| [List Legacy Video Groups](actions/list-legacy-video-groups.md) | GET | Retrieves legacy video groups from Reka AI. |
| [Move Videos To Group](actions/move-videos-to-group.md) | PUT | Updates video group membership in Reka AI. |
| [Move Videos To Legacy Group](actions/move-videos-to-legacy-group.md) | PUT | Updates legacy video group membership in Reka AI. |
| [Update Legacy Video Group](actions/update-legacy-video-group.md) | PUT | Updates an existing legacy video group in Reka AI. |
| [Update Video Group](actions/update-video-group.md) | PUT | Updates an existing video group in Reka AI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves models from Reka AI. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Transcribe or Translate Audio](actions/transcribe-or-translate-audio.md) | POST | Creates an audio transcription or translation in Reka AI. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Indexed Tag Video](actions/indexed-tag-video.md) | POST | Creates indexed tags for a video in Reka AI. |
| [Quick Tag Video](actions/quick-tag-video.md) | POST | Creates quick tags for a video in Reka AI. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature Catalog](actions/get-feature-catalog.md) | GET | Retrieves the feature catalog from Reka AI. |
| [List Captions](actions/list-captions.md) | GET | Retrieves captions from a Reka AI video. |
| [List Objects](actions/list-objects.md) | GET | Retrieves detected objects from a Reka AI video. |
| [List Scenes](actions/list-scenes.md) | GET | Retrieves scenes from a Reka AI video. |
| [List Transcript](actions/list-transcript.md) | GET | Retrieves a transcript from a Reka AI video. |
| [Plan Features](actions/plan-features.md) | POST | Creates a feature plan in Reka AI. |
| [Trigger Captions](actions/trigger-captions.md) | POST | Triggers caption generation for a video in Reka AI. |
| [Trigger Embeddings](actions/trigger-embeddings.md) | POST | Triggers embedding generation for a video in Reka AI. |
| [Trigger Objects](actions/trigger-objects.md) | POST | Triggers object detection for a video in Reka AI. |
| [Trigger Transcript](actions/trigger-transcript.md) | POST | Triggers transcript generation for a video in Reka AI. |

