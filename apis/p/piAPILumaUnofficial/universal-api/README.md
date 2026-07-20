# <img src="https://images.mindcloud.co/apps/icons/pi-api_1777067075774.png" alt="PiAPI/Luma (unofficial) logo" width="28" height="28"> PiAPI/Luma (unofficial): Universal API

Generate Luma videos and manage PiAPI video-generation tasks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPILumaUnofficial/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai/dream-machine-api
- **Vendor API docs:** https://piapi.ai/docs/doc-678694

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get PiAPI Account Info](actions/get-piapi-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Luma Task](actions/cancel-luma-task.md) | DELETE | Cancels an existing Luma task in PiAPI. |
| [Cancel Luma Tasks](actions/cancel-luma-tasks.md) | DELETE | Cancels Luma tasks in PiAPI created before a timestamp. |
| [Create Luma Task](actions/create-luma-task.md) | POST | Creates a new Luma task in PiAPI. |
| [Get Luma Task](actions/get-luma-task.md) | GET | Retrieves a Luma task from PiAPI. |
| [List PiAPI Luma Task History](actions/list-piapi-luma-task-history.md) | GET | Retrieves Luma task history from PiAPI. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get PiAPI Account Info](actions/get-piapi-account-info.md) | GET | Retrieves connected account details from PiAPI. |
| [Get PiAPI Active Tasks](actions/list-piapi-active-tasks.md) | GET | Retrieves active task counts from PiAPI. |

