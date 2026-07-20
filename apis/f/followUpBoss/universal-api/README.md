# <img src="https://images.mindcloud.co/apps/icons/ea913ec-small-fub-logo-mark-rgb-fub-logo-mark-main-small-1_1748980513130.png" alt="Follow Up Boss - Legacy logo" width="28" height="28"> Follow Up Boss - Legacy: Universal API

Manage real estate leads, tasks, appointments, and communication

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/followUpBoss/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.followupboss.com
- **Vendor API docs:** https://docs.followupboss.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from Follow Up Boss - Legacy. |
| [List People](actions/list-people.md) | GET | Retrieves people from Follow Up Boss - Legacy. |

