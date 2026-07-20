# <img src="https://images.mindcloud.co/apps/icons/pi-apiqwen_1776105815736.png" alt="PiAPI/Qwen logo" width="28" height="28"> PiAPI/Qwen: Universal API

Generate and edit images with Qwen and track tasks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIQwen/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Task](actions/get-task.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/get-task?connectionId=$CONNECTION_ID&task_id=task-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Image Edit Task](actions/create-image-edit-task.md) | POST | Creates an image edit task in PiAPI/Qwen. |
| [Create Text to Image Task](actions/create-text-to-image-task.md) | POST | Creates a text-to-image task in PiAPI/Qwen. |
| [Get Task](actions/get-task.md) | GET | Retrieves task status details from PiAPI/Qwen. |

