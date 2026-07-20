# <img src="https://images.mindcloud.co/apps/icons/tldv_1773171332831.png" alt="tl:dv logo" width="28" height="28"> tl:dv: Universal API

Manage meetings, transcripts, highlights, and imports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tldv/latest
- **Category:** Communication / Video Communications
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tldv.io
- **Vendor API docs:** https://doc.tldv.io/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Meetings](actions/list-meetings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/list-meetings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Highlight

| Action | Method | Description |
| --- | --- | --- |
| [Get Highlights](actions/get-highlights.md) | GET | Retrieves deprecated meeting highlights from tl:dv. |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting](actions/get-meeting.md) | GET | Retrieves a meeting from tl:dv. |
| [Import Meeting](actions/import-meeting.md) | POST | Imports a meeting into tl:dv from a URL. |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings from tl:dv. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a meeting transcript from tl:dv. |

