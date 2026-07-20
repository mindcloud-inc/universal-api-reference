# <img src="https://images.mindcloud.co/apps/icons/pi-apitoolkit_1776108611246.png" alt="PiAPI/Toolkit logo" width="28" height="28"> PiAPI/Toolkit: Universal API

Access PiAPI toolkit image and video utility endpoints through PiAPI's unified task API and account management surfaces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIToolkit/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [PiAPI Account Info](actions/piapi-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [File Upload API](actions/file-upload-api.md) | POST | Uploads a file for PiAPI/Toolkit tasks. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [PiAPI Account Info](actions/piapi-account-info.md) | GET | Retrieves account details from PiAPI/Toolkit. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Image Upscale - Get Task](actions/image-upscale-get-task.md) | GET | Retrieves an image-upscale task from PiAPI/Toolkit by ID. |
| [Image Upscale (Super Resolution) API](actions/image-upscale-super-resolution.md) | POST | Creates an image-upscale task in PiAPI/Toolkit. |
| [Remove Background API](actions/remove-background.md) | POST | Creates a background-removal task in PiAPI/Toolkit. |
| [Remove Background - Get Task](actions/remove-background-get-task.md) | GET | Retrieves a background-removal task from PiAPI/Toolkit by ID. |
| [Segment With Prompt API](actions/segment-with-prompt.md) | POST | Creates a prompt-based segmentation task in PiAPI/Toolkit. |
| [Segment With Prompt - Get Task](actions/segment-with-prompt-get-task.md) | GET | Retrieves a segmentation task from PiAPI/Toolkit by ID. |
| [Task List Info](actions/task-list-info.md) | GET | Retrieves active task counts from PiAPI/Toolkit. |
| [User Task History](actions/user-task-history.md) | GET | Retrieves user task history from PiAPI/Toolkit. |
| [Video Remove Background](actions/video-remove-background.md) | POST | Creates a video background-removal task in PiAPI/Toolkit. |
| [Video Remove Background - Get Task](actions/video-remove-background-get-task.md) | GET | Retrieves a video background-removal task from PiAPI/Toolkit by ID. |
| [Video Upscale](actions/video-upscale.md) | POST | Creates a video-upscale task in PiAPI/Toolkit. |
| [Video Upscale - Get Task](actions/video-upscale-get-task.md) | GET | Retrieves a video-upscale task from PiAPI/Toolkit by ID. |

