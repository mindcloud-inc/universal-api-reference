# <img src="https://images.mindcloud.co/apps/icons/full-session_1774908336795.png" alt="FullSession logo" width="28" height="28"> FullSession: Universal API

Replay sessions, analyze heatmaps, and understand website behavior

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fullSession/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fullsession.io
- **Vendor API docs:** https://help.fullsession.io/en/collections/14227501-apis-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Website Sessions](actions/list-website-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fullSession/latest/actions/list-website-sessions?connectionId=$CONNECTION_ID&customerId=string&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Session

| Action | Method | Description |
| --- | --- | --- |
| [List Website Sessions](actions/list-website-sessions.md) | GET | Retrieves website visitor sessions from FullSession. |

