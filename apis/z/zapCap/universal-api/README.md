# <img src="https://images.mindcloud.co/apps/icons/zap-cap_1774897855819.png" alt="ZapCap logo" width="28" height="28"> ZapCap: Universal API

Create captioned videos and viral clips with animated templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zapCap/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zapcap.ai
- **Vendor API docs:** https://platform.zapcap.ai/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Caption Task

| Action | Method | Description |
| --- | --- | --- |
| [Approve Transcript](actions/approve-transcript.md) | PUT | Approves a transcript for a ZapCap task. |
| [Create Auto-Approved Caption Task](actions/create-auto-approved-caption-task.md) | POST | Creates an auto-approved caption task in ZapCap. |
| [Create Caption Task](actions/create-caption-task.md) | POST | Creates a caption task in ZapCap. |
| [Create Review-Required Caption Task](actions/create-review-required-caption-task.md) | POST | Creates a review-required caption task in ZapCap. |
| [Get Caption Task Status](actions/get-caption-task-status.md) | GET | Retrieves caption task status from ZapCap. |

### Clip Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Long Clips](actions/create-long-clips.md) | POST | Creates a long clip task in ZapCap. |
| [Create Medium Clips](actions/create-medium-clips.md) | POST | Creates a medium clip task in ZapCap. |
| [Create Short Clips](actions/create-short-clips.md) | POST | Creates a short clip task in ZapCap. |
| [Create Viral Clips](actions/create-viral-clips.md) | POST | Creates a viral clip task in ZapCap. |
| [Get Viral Clip Task Status](actions/get-viral-clip-task-status.md) | GET | Retrieves clip task status from ZapCap. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Task](actions/create-video-task.md) | POST | Creates a video processing task in ZapCap. |
| [Get Video Task](actions/get-video-task.md) | GET | Retrieves a video task from ZapCap. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Fast Export](actions/create-fast-export.md) | POST | Creates a fast export task in ZapCap. |
| [Create Green Screen Export](actions/create-green-screen-export.md) | POST | Creates a green screen export task in ZapCap. |
| [Create Task With Auto Cut](actions/create-task-with-auto-cut.md) | POST | Creates a caption task in ZapCap with auto cut. |
| [Create Task With B-roll Percentage](actions/create-task-with-b-roll-percentage.md) | POST | Creates a caption task in ZapCap with B-roll coverage. |
| [Create Task With BYOT Transcript](actions/create-task-with-byot-transcript.md) | POST | Creates a caption task in ZapCap with a provided transcript. |
| [Create Task With Custom B-rolls](actions/create-task-with-custom-b-rolls.md) | POST | Creates a caption task in ZapCap with custom B-rolls. |
| [Create Task With Custom Styling](actions/create-task-with-custom-styling.md) | POST | Creates a caption task in ZapCap with custom styling. |
| [Create Task With Dictionary Hints](actions/create-task-with-dictionary-hints.md) | POST | Creates a caption task in ZapCap with dictionary hints. |
| [Create Task With Export Settings](actions/create-task-with-export-settings.md) | POST | Creates a caption task in ZapCap with export settings. |
| [Create Task With Reference Transcript](actions/create-task-with-reference-transcript.md) | POST | Creates a caption task in ZapCap with a reference transcript. |
| [Create Translated Subtitle Task](actions/create-translated-subtitle-task.md) | POST | Creates a translated subtitle task in ZapCap. |
| [Create 4K Export](actions/create4k-export.md) | POST | Creates a 4K export task in ZapCap. |
| [Create 60 FPS Export](actions/create60-fps-export.md) | POST | Creates a 60 FPS export task in ZapCap. |
| [Reuse Existing Transcript](actions/reuse-existing-transcript.md) | POST | Creates a caption task in ZapCap from an existing transcript. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves available templates from ZapCap. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from ZapCap. |
| [Upload Video](actions/upload-video.md) | POST | Uploads a video file to ZapCap. |
| [Upload Video By URL](actions/upload-video-by-url.md) | POST | Uploads a video to ZapCap from a public URL. |
| [Upload Video by URL (Mapped Field)](actions/upload-video-by-url-mapped-field.md) | POST | Uploads a video to ZapCap from a public URL. |

### Video Upload

| Action | Method | Description |
| --- | --- | --- |
| [Complete Multipart Upload](actions/complete-multipart-upload.md) | POST | Completes a multipart video upload in ZapCap. |
| [Start Multipart Upload](actions/start-multipart-upload.md) | POST | Starts a multipart video upload in ZapCap. |

