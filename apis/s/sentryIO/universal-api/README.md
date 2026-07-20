# <img src="https://images.mindcloud.co/apps/icons/sentry-io_1778189457022.png" alt="Sentry IO logo" width="28" height="28"> Sentry IO: Universal API

Monitor Sentry organizations, projects, issues, events, teams, releases, replays, and Explore data from MindCloud workflows and Cirra.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sentryIO/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sentry.io
- **Vendor API docs:** https://docs.sentry.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Your Organizations](actions/list-your-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-your-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Issue Events](actions/list-issue-events.md) | GET | Retrieves events for an issue in Sentry IO. |
| [List Project Error Events](actions/list-project-error-events.md) | GET | Retrieves error events from a Sentry IO project. |
| [Resolve Event ID](actions/resolve-event-id.md) | GET | Resolves a Sentry IO event ID to event details. |
| [Retrieve Issue Event](actions/retrieve-issue-event.md) | GET | Retrieves an event from a Sentry IO issue. |

### Explore Event Query

| Action | Method | Description |
| --- | --- | --- |
| [Query Explore Events](actions/query-explore-events.md) | GET | Queries table-format explore events in Sentry IO. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Issues](actions/list-organization-issues.md) | GET | Retrieves issues from a Sentry IO organization. |
| [Resolve Short ID](actions/resolve-short-id.md) | GET | Retrieves Sentry IO issue details by short ID. |
| [Retrieve Issue](actions/retrieve-issue.md) | GET | Retrieves an issue from Sentry IO. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Sentry IO. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves members from a Sentry IO organization. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves members from a Sentry IO team. |
| [Retrieve Organization Member](actions/retrieve-organization-member.md) | GET | Retrieves an organization member from Sentry IO. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Your Organizations](actions/list-your-organizations.md) | GET | Retrieves your organizations from Sentry IO. |
| [Retrieve Organization](actions/retrieve-organization.md) | GET | Retrieves an organization from Sentry IO. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Projects](actions/list-organization-projects.md) | GET | Retrieves projects from a Sentry IO organization. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a project from Sentry IO. |

### Project Event Count

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Project Event Counts](actions/retrieve-project-event-counts.md) | GET | Retrieves project event counts from Sentry IO. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Releases](actions/list-organization-releases.md) | GET | Retrieves releases from a Sentry IO organization. |
| [Retrieve Organization Release](actions/retrieve-organization-release.md) | GET | Retrieves an organization release from Sentry IO. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Teams](actions/list-organization-teams.md) | GET | Retrieves teams from a Sentry IO organization. |
| [Retrieve Team](actions/retrieve-team.md) | GET | Retrieves a team from Sentry IO. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Project Users](actions/list-project-users.md) | GET | Retrieves users from a Sentry IO project. |

