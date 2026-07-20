# <img src="https://images.mindcloud.co/apps/icons/pi-api_1777065266436.png" alt="PiAPI/DiffRhythm logo" width="28" height="28"> PiAPI/DiffRhythm: Universal API

Create DiffRhythm music-generation tasks, upload reference audio for style guidance, and check PiAPI task and account status.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIDiffRhythm/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/diffrhythm-api/create-task

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [PiAPI Account Info](actions/piapi-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIDiffRhythm/latest/actions/piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [File Upload API](actions/file-upload-api.md) | POST | Creates a temporary file upload in PiAPI/DiffRhythm. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [PiAPI Account Info](actions/piapi-account-info.md) | GET | Retrieves your account information from PiAPI/DiffRhythm. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Generate Audio](actions/generate-audio.md) | POST | Creates a DiffRhythm audio task in PiAPI/DiffRhythm. |
| [Get Task](actions/get-task.md) | GET | Retrieves a DiffRhythm task from PiAPI/DiffRhythm. |
| [Task List Info](actions/task-list-info.md) | GET | Retrieves active task information from PiAPI/DiffRhythm. |
| [User Task History](actions/user-task-history.md) | GET | Retrieves your task history from PiAPI/DiffRhythm. |

