# <img src="https://images.mindcloud.co/apps/icons/316-3168671-companies-dont-really-use-illustrations-like-this-fogbugz-logo_1774375820005.png" alt="FogBugz logo" width="28" height="28"> FogBugz: Universal API

Track cases, manage projects, and support software teams

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fogBugz/latest
- **Category:** Productivity / Project Management
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trial.fogbugz.com
- **Vendor API docs:** https://support.fogbugz.com/en-us/article/55730-fogbugz-api-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [List Cases](actions/list-cases.md) | GET | Retrieves cases from FogBugz. |
| [View Case](actions/view-case.md) | GET | Retrieves case details from FogBugz. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from FogBugz. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from FogBugz. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves milestones from FogBugz. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from FogBugz. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Areas](actions/list-areas.md) | GET | Retrieves areas from FogBugz. |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves mailboxes from FogBugz. |
| [List Priorities](actions/list-priorities.md) | GET | Retrieves priorities from FogBugz. |
| [List Wikis](actions/list-wikis.md) | GET | Retrieves wikis from FogBugz. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List People](actions/list-people.md) | GET | Retrieves people from FogBugz. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [List Filters](actions/list-filters.md) | GET | Retrieves filters from FogBugz. |

