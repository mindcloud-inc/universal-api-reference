# ZapCap: Native API Reference

A consolidated summary of ZapCap's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://platform.zapcap.ai/docs/api
- **API base URL:** `https://api.zapcap.ai`

## Authentication

### API Key

Connect with your ZapCap API key from the ZapCap dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://platform.zapcap.ai/docs/quickstart/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Transcript](actions/approve-transcript.md) | `POST /videos/:videoId/task/:id/approve-transcript` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task/%7Bid%7D/approve-transcript) |
| [Complete Multipart Upload](actions/complete-multipart-upload.md) | `POST /videos/upload/complete` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/upload/complete) |
| [Create Auto-Approved Caption Task](actions/create-auto-approved-caption-task.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Caption Task](actions/create-caption-task.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Fast Export](actions/create-fast-export.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Green Screen Export](actions/create-green-screen-export.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Long Clips](actions/create-long-clips.md) | `POST /videos/:videoId/clipTask` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/clipTask) |
| [Create Medium Clips](actions/create-medium-clips.md) | `POST /videos/:videoId/clipTask` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/clipTask) |
| [Create Review-Required Caption Task](actions/create-review-required-caption-task.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Short Clips](actions/create-short-clips.md) | `POST /videos/:videoId/clipTask` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/clipTask) |
| [Create Task With Auto Cut](actions/create-task-with-auto-cut.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With B-roll Percentage](actions/create-task-with-b-roll-percentage.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With BYOT Transcript](actions/create-task-with-byot-transcript.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With Custom B-rolls](actions/create-task-with-custom-b-rolls.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With Custom Styling](actions/create-task-with-custom-styling.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With Dictionary Hints](actions/create-task-with-dictionary-hints.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With Export Settings](actions/create-task-with-export-settings.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Task With Reference Transcript](actions/create-task-with-reference-transcript.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Translated Subtitle Task](actions/create-translated-subtitle-task.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Video Task](actions/create-video-task.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create Viral Clips](actions/create-viral-clips.md) | `POST /videos/:videoId/clipTask` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/clipTask) |
| [Create 4K Export](actions/create4k-export.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Create 60 FPS Export](actions/create60-fps-export.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Get Caption Task Status](actions/get-caption-task-status.md) | `GET /videos/:videoId/task/:id` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/get/videos/%7BvideoId%7D/task/%7Bid%7D) |
| [Get Video Task](actions/get-video-task.md) | `GET /videos/:videoId/task/:id` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/get/videos/%7BvideoId%7D/task/%7Bid%7D) |
| [Get Viral Clip Task Status](actions/get-viral-clip-task-status.md) | `GET /videos/:videoId/clipTask/:id` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/get/videos/%7BvideoId%7D/clipTask/%7Bid%7D) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://platform.zapcap.ai/docs/api#tag/templates/get/templates) |
| [List Videos](actions/list-videos.md) | `GET /videos` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/get/videos) |
| [Reuse Existing Transcript](actions/reuse-existing-transcript.md) | `POST /videos/:videoId/task` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/%7BvideoId%7D/task) |
| [Start Multipart Upload](actions/start-multipart-upload.md) | `POST /videos/upload` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/upload) |
| [Upload Video](actions/upload-video.md) | `POST /videos` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos) |
| [Upload Video By URL](actions/upload-video-by-url.md) | `POST /videos/url` | [docs](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/url) |
