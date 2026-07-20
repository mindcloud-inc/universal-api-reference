# <img src="https://images.mindcloud.co/apps/icons/pi-apisora_1776105878762.png" alt="PiAPI/Sora logo" width="28" height="28"> PiAPI/Sora: Universal API

Use PiAPI Sora endpoints to create and track Sora video-generation tasks from text prompts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPISora/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/sora2-api/text-to-video

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get PiAPI Account Info](actions/get-piapi-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/get-piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Sora2 Pro Text to Video Task](actions/create-sora2-pro-text-to-video-task.md) | POST |  |
| [Create Sora2 Text to Video Task](actions/create-sora2-text-to-video-task.md) | POST |  |
| [Get Sora2 Task](actions/get-sora2-task.md) | GET |  |
| [Remove Watermark from Sora2 Video](actions/remove-watermark-from-sora2-video.md) | POST |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get PiAPI Account Info](actions/get-piapi-account-info.md) | GET |  |

