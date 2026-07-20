# <img src="https://images.mindcloud.co/apps/icons/pi-apiqwen-1776105815736_1776109602760.png" alt="PiAPI/MMAudio logo" width="28" height="28"> PiAPI/MMAudio: Universal API

Generate audio from video and track PiAPI MMAudio tasks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIMMAudio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Task](actions/get-task.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=task%20identifier%20returned%20by%20Generate%20Audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Generate Audio](actions/generate-audio.md) | POST | Creates an MMAudio audio generation task in PiAPI/MMAudio. |
| [Get Task](actions/get-task.md) | GET | Retrieves an MMAudio task from PiAPI/MMAudio. |

