# <img src="https://images.mindcloud.co/apps/icons/domo-ai_1774962123318.png" alt="DomoAI logo" width="28" height="28"> DomoAI: Universal API

AI-powered video generation API for text-to-video, image-to-video, template-based video, talking avatar, video-to-video, file upload, and async task polling workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/domoAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.domoai.app
- **Vendor API docs:** https://docs.domoai.app/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Task](actions/get-task.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Creates a new file upload slot in DomoAI. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Image to Video Task](actions/create-image-to-video-task.md) | POST | Creates a new image-to-video task in DomoAI. |
| [Create Talking Avatar Task](actions/create-talking-avatar-task.md) | POST | Creates a new talking avatar task in DomoAI. |
| [Create Template to Video Task](actions/create-template-to-video-task.md) | POST | Creates a new template-to-video task in DomoAI. |
| [Create Text to Video Task](actions/create-text-to-video-task.md) | POST | Creates a new text-to-video task in DomoAI. |
| [Create Video to Video Task](actions/create-video-to-video-task.md) | POST | Creates a new video-to-video task in DomoAI. |
| [Get Task](actions/get-task.md) | GET | Retrieves task status and outputs from DomoAI. |

