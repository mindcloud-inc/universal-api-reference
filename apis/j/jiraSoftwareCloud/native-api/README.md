# Jira Software Cloud: Native API Reference

A consolidated summary of Jira Software Cloud's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/
- **OpenAPI specification:** https://developer.atlassian.com/cloud/jira/platform/swagger.v3.json
- **API base URL:** `https://api.atlassian.com`

## Authentication

### OAuth 2.0

Atlassian OAuth 2.0 (3LO) for Jira Software Cloud.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.atlassian.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.atlassian.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read:jira-user read:jira-work write:jira-work offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.atlassian.com/oauth/token.

[Official authentication documentation](https://developer.atlassian.com/cloud/jira/platform/oauth-2-3lo-apps/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `maxResults` in the query string to set the page size. Use `startAt` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accessible Resources](actions/accessible-resources.md) | `GET /oauth/token/accessible-resources` | [docs](https://developer.atlassian.com/cloud/jira/platform/oauth-2-3lo-apps/) |
| [Add Comment](actions/add-comment.md) | `POST /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/) |
| [Assign Issue](actions/assign-issue.md) | `PUT /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/assignee` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Count Issues Using JQL](actions/count-issues-using-jql.md) | `POST /ex/jira/:cloudId/rest/api/3/search/approximate-count` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-search/) |
| [Create Issue](actions/create-issue.md) | `POST /ex/jira/:cloudId/rest/api/3/issue` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/) |
| [Delete Issue](actions/delete-issue.md) | `DELETE /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Edit Issue](actions/edit-issue.md) | `PUT /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Get Comment](actions/get-comment.md) | `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/) |
| [Get Comments](actions/get-comments.md) | `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/) |
| [Get Create Metadata Issue Types For Project](actions/get-create-metadata-issue-types-for-project.md) | `GET /ex/jira/:cloudId/rest/api/3/issue/createmeta/:projectIdOrKey/issuetypes` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Get Current User](actions/get-current-user.md) | `GET /ex/jira/:cloudId/rest/api/3/myself` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-myself/) |
| [Get Issue](actions/get-issue.md) | `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Get Project](actions/get-project.md) | `GET /ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/) |
| [Get Project Components Paginated](actions/get-project-components-paginated.md) | `GET /ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey/component` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-project-components/) |
| [Get Project Statuses](actions/get-project-statuses.md) | `GET /ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey/statuses` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/) |
| [Get Project Versions Paginated](actions/get-project-versions-paginated.md) | `GET /ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey/version` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-project-versions/) |
| [Get Projects Paginated](actions/get-projects-paginated.md) | `GET /ex/jira/:cloudId/rest/api/3/project/search` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/) |
| [Get Transitions](actions/get-transitions.md) | `GET /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/transitions` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Get User](actions/get-user.md) | `GET /ex/jira/:cloudId/rest/api/3/user` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-users/) |
| [Search Issues Using JQL Enhanced Search (GET)](actions/search-issues-using-jql-enhanced-search-get.md) | `GET /ex/jira/:cloudId/rest/api/3/search/jql` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-search/) |
| [Search Issues Using JQL Enhanced Search (POST)](actions/search-issues-using-jql-enhanced-search-post.md) | `POST /ex/jira/:cloudId/rest/api/3/search/jql` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-search/) |
| [Transition Issue](actions/transition-issue.md) | `POST /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/transitions` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issues/) |
| [Update Comment](actions/update-comment.md) | `PUT /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey/comment/:id` | [docs](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-comments/) |
