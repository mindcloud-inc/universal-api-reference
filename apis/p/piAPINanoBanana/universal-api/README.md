# <img src="https://images.mindcloud.co/apps/icons/pi-apiqwen-1776105815736_1776109594770.png" alt="PiAPI/NanoBanana logo" width="28" height="28"> PiAPI/NanoBanana: Universal API

Create and track PiAPI Nano Banana image generation tasks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPINanoBanana/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPINanoBanana/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Gemini 2.5 Flash Image Task](actions/create-gemini25-flash-image-task.md) | POST |  |
| [Create Nano Banana Pro Task](actions/create-nano-banana-pro-task.md) | POST |  |
| [Create Nano Banana 2 Task](actions/create-nano-banana2-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Active Tasks](actions/list-active-tasks.md) | GET |  |
| [List User Task History](actions/list-user-task-history.md) | GET |  |

