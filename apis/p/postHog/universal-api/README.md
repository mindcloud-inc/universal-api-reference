# <img src="https://images.mindcloud.co/apps/icons/image-2840-vectorized_1777471197999.png" alt="PostHog logo" width="28" height="28"> PostHog: Universal API

Analyze product usage, replay sessions, run experiments, and capture events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postHog/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://posthog.com/
- **Vendor API docs:** https://posthog.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Log](actions/list-activity-log.md) | GET | Retrieves activity log entries from a PostHog project. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from PostHog. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Persons](actions/list-persons.md) | GET | Retrieves persons from a PostHog project. |

### Organization Invite

| Action | Method | Description |
| --- | --- | --- |
| [Add or Invite Members](actions/add-or-invite-members.md) | POST | Creates an organization invite in PostHog. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a PostHog organization. |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Query](actions/query.md) | GET | Retrieves query results from a PostHog project. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Recording](actions/get-session-recording.md) | GET | Retrieves a session recording from a PostHog project. |
| [List Session Recordings](actions/list-session-recordings.md) | GET | Retrieves session recordings from a PostHog project. |

