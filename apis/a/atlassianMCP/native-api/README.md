# Atlassian MCP: Native API Reference

A consolidated summary of Atlassian MCP's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/
- **API base URL:** `https://mcp.atlassian.com/v1`

## Authentication

### Atlassian Personal API Token

Personal Atlassian scoped API token for Atlassian MCP access. Uses your Atlassian account email plus the scoped token value.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/configuring-authentication-via-api-token/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |
| `Content-Type` | `application/json` |

Response formats vary by operation and include plain text and JSON. Response data is read from `response`.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confluence - Create Footer Comment](actions/confluence-create-footer-comment.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - Create Inline Comment](actions/confluence-create-inline-comment.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - Create Page](actions/confluence-create-page.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - Get Page](actions/confluence-get-page.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - List Page Descendants](actions/confluence-list-page-descendants.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - List Space Pages](actions/confluence-list-space-pages.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - List Spaces](actions/confluence-list-spaces.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - Search Pages](actions/confluence-search-pages.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Confluence - Update Page](actions/confluence-update-page.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools) |
| [Initialize Session](actions/initialize-session.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-with-other-supported-mcp-clients/) |
| [Jira - Add Comment](actions/jira-add-comment.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Add Worklog](actions/jira-add-worklog.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Create Issue](actions/jira-create-issue.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Edit Issue](actions/jira-edit-issue.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Get Issue](actions/jira-get-issue.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - List Issue Transitions](actions/jira-list-issue-transitions.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - List Project Issue Types](actions/jira-list-project-issue-types.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - List Visible Projects](actions/jira-list-visible-projects.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Lookup Account ID](actions/jira-lookup-account-id.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Search Issues](actions/jira-search-issues.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [Jira - Transition Issue](actions/jira-transition-issue.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools) |
| [List Tools](actions/list-tools.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/) |
| [Notify Initialized](actions/notify-initialized.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-with-other-supported-mcp-clients/) |
| [Shared Platform - Fetch](actions/shared-platform-fetch.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-rovo-search-and-fetch-in-the-atlassian-remote-mcp-server/) |
| [Shared Platform - Get Current User](actions/shared-platform-get-current-user.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Rovo-code---Shared-platform-tools) |
| [Shared Platform - List Accessible Resources](actions/shared-platform-list-accessible-resources.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Rovo-code---Shared-platform-tools) |
| [Shared Platform - Search](actions/shared-platform-search.md) | `POST /mcp` | [docs](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-rovo-search-and-fetch-in-the-atlassian-remote-mcp-server/) |
