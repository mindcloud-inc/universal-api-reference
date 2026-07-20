# <img src="https://images.mindcloud.co/apps/icons/65db514e1a37a328eaee4b6c-pagerly-logo-256_1774977754067.png" alt="Pagerly logo" width="28" height="28"> Pagerly: Universal API

Manage on-call teams and fetch current on-call users from Pagerly rotation schedules.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pagerly/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pagerly.io
- **Vendor API docs:** https://docs.pagerly.io/api/rotations-endpoint

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves on-call teams from Pagerly. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current On-Call Jira Account](actions/get-current-on-call-jira-account.md) | GET | Retrieves the current on-call Jira account from Pagerly. |
| [List Current On-Call Users](actions/list-current-on-call-users.md) | GET | Retrieves current on-call users from Pagerly. |

