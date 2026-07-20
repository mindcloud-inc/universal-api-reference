# <img src="https://images.mindcloud.co/apps/icons/jira-software_1776890925197.png" alt="Jira Software Cloud logo" width="28" height="28"> Jira Software Cloud: Universal API

Jira Software Cloud integration for issues, comments, projects, users, and related Jira REST workflows using Atlassian OAuth 2.0.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jiraSoftwareCloud/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.atlassian.com/software/jira
- **Vendor API docs:** https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Accessible Resources](actions/accessible-resources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/accessible-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a new comment in Jira Software Cloud. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Jira Software Cloud. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Jira Software Cloud. |
| [Get Comments](actions/get-comments.md) | GET | Retrieves issue comments from Jira Software Cloud. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Jira Software Cloud. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Components Paginated](actions/get-project-components-paginated.md) | GET | Retrieves project components from Jira Software Cloud. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Assign Issue](actions/assign-issue.md) | PUT | Updates an issue assignee in Jira Software Cloud. |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Jira Software Cloud. |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Jira Software Cloud. |
| [Edit Issue](actions/edit-issue.md) | PUT | Updates an existing issue in Jira Software Cloud. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from Jira Software Cloud. |
| [Search Issues Using JQL Enhanced Search (GET)](actions/search-issues-using-jql-enhanced-search-get.md) | GET | Finds issues in Jira Software Cloud using JQL. |
| [Search Issues Using JQL Enhanced Search (POST)](actions/search-issues-using-jql-enhanced-search-post.md) | GET | Finds issues in Jira Software Cloud using JQL. |
| [Transition Issue](actions/transition-issue.md) | PUT | Transitions an issue in Jira Software Cloud. |

### Issue Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Issues Using JQL](actions/count-issues-using-jql.md) | GET | Retrieves an approximate JQL issue count from Jira Software Cloud. |

### Issue Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Create Metadata Issue Types For Project](actions/get-create-metadata-issue-types-for-project.md) | GET | Retrieves project issue types for Jira Software Cloud issue creation. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Jira Software Cloud. |
| [Get Projects Paginated](actions/get-projects-paginated.md) | GET | Retrieves projects from Jira Software Cloud. |

### Project Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Statuses](actions/get-project-statuses.md) | GET | Retrieves project statuses from Jira Software Cloud. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Accessible Resources](actions/accessible-resources.md) | GET | Retrieves accessible Jira Software Cloud sites for this token. |

### Transition

| Action | Method | Description |
| --- | --- | --- |
| [Get Transitions](actions/get-transitions.md) | GET | Retrieves issue transitions from Jira Software Cloud. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current Jira Software Cloud user. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Jira Software Cloud. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Versions Paginated](actions/get-project-versions-paginated.md) | GET | Retrieves project versions from Jira Software Cloud. |

