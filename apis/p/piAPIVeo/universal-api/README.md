# <img src="https://images.mindcloud.co/apps/icons/pi-apiveo_1776104269188.png" alt="PiAPI/Veo logo" width="28" height="28"> PiAPI/Veo: Universal API

Generate Veo videos and track PiAPI task status

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIVeo/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai/veo-3
- **Vendor API docs:** https://piapi.ai/docs/doc-678694

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account information from PiAPI/Veo. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Veo3 Image to Video Task](actions/create-veo3-image-to-video-task.md) | POST | Creates a Veo 3 image-to-video task in PiAPI/Veo. |
| [Create Veo3 Text to Video Task](actions/create-veo3-text-to-video-task.md) | POST | Creates a Veo 3 text-to-video task in PiAPI/Veo. |
| [Create Veo3.1 Image to Video Task](actions/create-veo31-image-to-video-task.md) | POST | Creates a Veo 3.1 image-to-video task in PiAPI/Veo. |
| [Create Veo3.1 Text to Video Task](actions/create-veo31-text-to-video-task.md) | POST | Creates a Veo 3.1 text-to-video task in PiAPI/Veo. |
| [Get Task](actions/get-task.md) | GET | Retrieves a Veo task from PiAPI/Veo by ID. |
| [List Active Tasks](actions/list-active-tasks.md) | GET | Retrieves active tasks from PiAPI/Veo. |
| [List User Task History](actions/list-user-task-history.md) | GET | Retrieves user task history from PiAPI/Veo. |

