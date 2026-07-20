# <img src="https://images.mindcloud.co/apps/icons/rendi_1775148542648.png" alt="Rendi logo" width="28" height="28"> Rendi: Universal API

Run FFmpeg and FFprobe jobs through Rendi's cloud API with asynchronous polling and hosted file outputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rendi/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rendi.dev
- **Vendor API docs:** https://docs.rendi.dev/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List FFmpeg Commands](actions/list-f-fmpeg-commands.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-f-fmpeg-commands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a stored file from Rendi. |
| [Delete Files in Bulk](actions/delete-files-in-bulk.md) | DELETE | Deletes multiple stored files from Rendi. |
| [Get File](actions/get-file.md) | GET | Retrieves a stored file from Rendi. |
| [List Stored Files](actions/list-stored-files.md) | GET | Retrieves stored account files from Rendi. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Delete Command Files](actions/delete-command-files.md) | DELETE | Deletes stored output files for a command in Rendi. |
| [List FFmpeg Commands](actions/list-f-fmpeg-commands.md) | GET | Retrieves submitted FFmpeg commands from Rendi. |
| [Poll FFmpeg Command](actions/poll-f-fmpeg-command.md) | GET | Retrieves the status of an FFmpeg command in Rendi. |
| [Run FFmpeg Command](actions/run-f-fmpeg-command.md) | POST | Submits an FFmpeg command for processing in Rendi. |

