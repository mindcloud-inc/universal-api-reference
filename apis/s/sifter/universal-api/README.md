# <img src="https://images.mindcloud.co/apps/icons/sifter_1774470301671.png" alt="Sifter logo" width="28" height="28"> Sifter: Universal API

Sifter is a simple issue tracker for teams that need straightforward bug and issue tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sifter/latest
- **Category:** Support / Ticketing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sifterapp.com
- **Vendor API docs:** https://sifterapp.com/developer/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Project Categories](actions/list-project-categories.md) | GET | Retrieves categories for a project from Sifter. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment on a Sifter issue. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Sifter. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves a specific issue from Sifter. |
| [List Issues](actions/list-issues.md) | GET | Retrieves issues for a project from Sifter. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Project Milestones](actions/list-project-milestones.md) | GET | Retrieves milestones for a project from Sifter. |

### Priority

| Action | Method | Description |
| --- | --- | --- |
| [List Priorities](actions/list-priorities.md) | GET | Retrieves available issue priorities from Sifter. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a specific project from Sifter. |
| [List Projects](actions/list-projects.md) | GET | Retrieves accessible open projects from Sifter. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Metadata](actions/get-project-metadata.md) | GET | Retrieves detailed project metadata from Sifter. |
| [List All Projects](actions/list-all-projects.md) | GET | Retrieves all accessible projects from Sifter. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Project Statuses](actions/list-project-statuses.md) | GET | Retrieves statuses for a project from Sifter. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Sifter. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Project People](actions/list-project-people.md) | GET | Retrieves assigned people for a project from Sifter. |

