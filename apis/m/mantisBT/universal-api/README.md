# <img src="https://images.mindcloud.co/apps/icons/mantis-bt_1776267873852.png" alt="MantisBT logo" width="28" height="28"> MantisBT: Universal API

MantisBT is an open-source issue tracker for managing bugs, projects, users, filters, and related issue data through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mantisBT/latest
- **Category:** Productivity / Project Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mantisbt.org
- **Vendor API docs:** https://github.com/mantisbt/mantisbt/blob/master/api/rest/mantisbt_openapi.yaml

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My User Info](actions/get-my-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-my-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Configuration Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Configuration Options](actions/get-configuration-options.md) | GET | Retrieves configuration options from MantisBT by key. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in MantisBT. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from MantisBT by ID. |
| [Get Issues](actions/get-issues.md) | GET | Retrieves issues from your MantisBT workspace. |
| [Monitor Issue](actions/monitor-issue.md) | PUT | Adds monitoring to an issue in MantisBT. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in MantisBT. |

### Issue Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue Note](actions/create-issue-note.md) | POST | Creates a new issue note in MantisBT. |
| [Delete Issue Note](actions/delete-issue-note.md) | DELETE | Deletes an issue note from MantisBT. |

### Localized String

| Action | Method | Description |
| --- | --- | --- |
| [Get Localized Strings](actions/get-localized-strings.md) | GET | Retrieves localized strings from MantisBT by key. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from MantisBT by ID. |
| [Get Projects](actions/get-projects.md) | GET | Retrieves available projects from the MantisBT workspace. |

### Project Version

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Version](actions/create-project-version.md) | POST | Creates a new project version in MantisBT. |
| [Delete Project Version](actions/delete-project-version.md) | DELETE | Deletes a project version from MantisBT. |
| [Get Project Version](actions/get-project-version.md) | GET | Retrieves a project version from MantisBT. |
| [Get Project Versions](actions/get-project-versions.md) | GET | Retrieves project versions from a MantisBT project. |
| [Update Project Version](actions/update-project-version.md) | PUT | Updates an existing project version in MantisBT. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My User Info](actions/get-my-user-info.md) | GET | Retrieves the current user from MantisBT. |
| [Get Project Handlers](actions/get-project-handlers.md) | GET | Retrieves available project handlers from MantisBT. |
| [Get Project Users](actions/get-project-users.md) | GET | Retrieves project users from a MantisBT project. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from MantisBT by ID. |
| [Get User By Username](actions/get-user-by-username.md) | GET | Finds a user in MantisBT by username. |

