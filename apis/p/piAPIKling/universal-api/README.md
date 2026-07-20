# <img src="https://images.mindcloud.co/apps/icons/pi-api_1777067508469.png" alt="PiAPI/Kling logo" width="28" height="28"> PiAPI/Kling: Universal API

Create and manage PiAPI Kling video, audio, avatar, motion-control, effects, and try-on tasks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIKling/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/kling-api/create-task

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET |  |

### Cancellation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Task](actions/cancel-task.md) | DELETE |  |
| [Cancel Tasks Before Timestamp](actions/cancel-tasks-before-timestamp.md) | DELETE |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Generate Avatar Video](actions/generate-avatar-video.md) | POST |  |
| [Generate Effects Video](actions/generate-effects-video.md) | POST |  |
| [Generate Elements Video](actions/generate-elements-video.md) | POST |  |
| [Generate Motion Control Video](actions/generate-motion-control-video.md) | POST |  |
| [Generate Omni Video](actions/generate-omni-video.md) | POST |  |
| [Generate Sound](actions/generate-sound.md) | POST |  |
| [Generate Turbo Video](actions/generate-turbo-video.md) | POST |  |
| [Generate Video from Image](actions/generate-video-from-image.md) | POST |  |
| [Generate Video from Text](actions/generate-video-from-text.md) | POST |  |
| [Generate Virtual Try-On](actions/generate-virtual-try-on.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Lip Sync Video](actions/lip-sync-video.md) | POST |  |
| [List Active Tasks](actions/list-active-tasks.md) | GET |  |

### Task History

| Action | Method | Description |
| --- | --- | --- |
| [List User Task History](actions/list-user-task-history.md) | GET |  |

