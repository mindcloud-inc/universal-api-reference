# <img src="https://images.mindcloud.co/apps/icons/pi-apiqwen-1776105815736_1776109590584.png" alt="PiAPI/Trellis logo" width="28" height="28"> PiAPI/Trellis: Universal API

PiAPI Trellis exposes Trellis and Trellis2 3D generation through PiAPI's unified task create/get endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPITrellis/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/trellis-api/create-task

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your account information from PiAPI/Trellis. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Trellis Image-to-3D Task](actions/create-trellis-image-to-3d-task.md) | POST | Creates a Trellis image-to-3D task in PiAPI/Trellis. |
| [Create Trellis Text-to-3D Task](actions/create-trellis-text-to-3d-task.md) | POST | Creates a Trellis text-to-3D task in PiAPI/Trellis. |
| [Create Trellis2 Image-to-3D Task](actions/create-trellis2-image-to-3d-task.md) | POST | Creates a Trellis2 image-to-3D task in PiAPI/Trellis. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from PiAPI/Trellis. |
| [List Active Tasks](actions/list-active-tasks.md) | GET | Retrieves active tasks from PiAPI/Trellis. |
| [List Task History](actions/list-task-history.md) | GET | Retrieves your task history from PiAPI/Trellis. |

