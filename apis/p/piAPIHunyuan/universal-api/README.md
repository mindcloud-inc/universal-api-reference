# <img src="https://images.mindcloud.co/apps/icons/pi-api_1777067121385.png" alt="PiAPI/Hunyuan logo" width="28" height="28"> PiAPI/Hunyuan: Universal API

Generate Hunyuan videos and monitor PiAPI task status

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIHunyuan/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai/hunyuan
- **Vendor API docs:** https://piapi.ai/docs/hunyuan-video/txt2video-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Active Tasks](actions/list-active-tasks.md) | GET |  |
| [List User Task History](actions/list-user-task-history.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Fast Text to Video Task](actions/create-fast-text-to-video-task.md) | POST |  |
| [Create Image to Video (Concat) Task](actions/create-image-to-video-concat-task.md) | POST |  |
| [Create Image to Video (Replace) Task](actions/create-image-to-video-replace-task.md) | POST |  |
| [Create Text to Video Task](actions/create-text-to-video-task.md) | POST |  |
| [Create Text to Video with LoRA Task](actions/create-text-to-video-with-lo-ra-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |

