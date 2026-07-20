# <img src="https://images.mindcloud.co/apps/icons/fathom_1772559201868.png" alt="Fathom logo" width="28" height="28"> Fathom: Universal API

Record meetings, generate summaries, sync notes, and track follow-ups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fathom/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fathom.video
- **Vendor API docs:** https://developers.fathom.ai/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Meetings](actions/list-meetings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Fathom. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Fathom. |
| [Get Recording Summary](actions/get-recording-summary.md) | GET | Retrieves a recording summary from Fathom. |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a transcript from Fathom. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Fathom. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Fathom. |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings from Fathom. |

