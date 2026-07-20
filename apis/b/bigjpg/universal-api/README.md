# <img src="https://images.mindcloud.co/apps/icons/bigjpg_1776794340512.png" alt="Bigjpg logo" width="28" height="28"> Bigjpg: Universal API

Bigjpg is an AI image upscaling service for enlarging images while reducing noise and preserving detail.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigjpg/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bigjpg.com/
- **Vendor API docs:** https://bigjpg.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Task Result](actions/get-task-result.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/get-task-result?connectionId=$CONNECTION_ID&taskIds=tid1%2Ctid2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Enlarge Task](actions/create-enlarge-task.md) | POST | Creates an image enlargement task in Bigjpg. |
| [Get Task Result](actions/get-task-result.md) | GET | Retrieves task results from Bigjpg by task ID. |
| [Retry Task](actions/retry-task.md) | PUT | Retries image enlargement tasks in Bigjpg by task ID. |

