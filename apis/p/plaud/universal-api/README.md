# <img src="https://images.mindcloud.co/apps/icons/favicon-www-plaud-ai-64x64_1794843265446.png" alt="Plaud AI logo" width="28" height="28"> Plaud AI: Universal API

Browse Plaud recordings and retrieve audio links, transcripts, notes, and account details.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/plaud/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.plaud.ai
- **Vendor API docs:** https://docs.plaud.ai/plaud-mcp-cli/mcp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Notes](actions/get-notes.md) | GET |  |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Get Recording](actions/get-recording.md) | GET |  |
| [List Recordings](actions/list-recordings.md) | GET |  |

### Transcripts

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcript](actions/get-transcript.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

