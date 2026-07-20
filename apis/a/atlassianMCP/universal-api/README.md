# <img src="https://images.mindcloud.co/apps/icons/atlassian_1774030532889.png" alt="Atlassian MCP logo" width="28" height="28"> Atlassian MCP: Universal API

Search Atlassian content and manage Jira and Confluence work

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/atlassianMCP/latest
- **Category:** Productivity / Project Management
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.atlassian.com/rovo
- **Vendor API docs:** https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Initialize Session](actions/initialize-session.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/initialize-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Confluence - Create Footer Comment](actions/confluence-create-footer-comment.md) | POST | Creates a Confluence footer comment in Atlassian MCP. |
| [Confluence - Create Inline Comment](actions/confluence-create-inline-comment.md) | POST | Creates a Confluence inline comment in Atlassian MCP. |
| [Jira - Add Comment](actions/jira-add-comment.md) | POST | Adds a comment to a Jira issue in Atlassian MCP. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Shared Platform - Fetch](actions/shared-platform-fetch.md) | GET | Fetches Jira or Confluence content by ARI in Atlassian MCP. |

### Issue Types

| Action | Method | Description |
| --- | --- | --- |
| [Jira - List Project Issue Types](actions/jira-list-project-issue-types.md) | GET | Retrieves Jira project issue types from Atlassian MCP. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Jira - Create Issue](actions/jira-create-issue.md) | POST | Creates a Jira issue in Atlassian MCP. |
| [Jira - Edit Issue](actions/jira-edit-issue.md) | PUT | Updates a Jira issue in Atlassian MCP. |
| [Jira - Get Issue](actions/jira-get-issue.md) | GET | Retrieves a Jira issue by ID or key from Atlassian MCP. |
| [Jira - Search Issues](actions/jira-search-issues.md) | GET | Searches Jira issues by JQL in Atlassian MCP. |
| [Jira - Transition Issue](actions/jira-transition-issue.md) | PUT | Transitions a Jira issue in Atlassian MCP. |

### Mcp Session

| Action | Method | Description |
| --- | --- | --- |
| [Initialize Session](actions/initialize-session.md) | GET | Initializes an Atlassian MCP session. |
| [Notify Initialized](actions/notify-initialized.md) | GET | Sends the MCP initialized notification to Atlassian MCP. |

### Mcp Tool

| Action | Method | Description |
| --- | --- | --- |
| [List Tools](actions/list-tools.md) | GET | Retrieves supported Atlassian MCP tools. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Confluence - Create Page](actions/confluence-create-page.md) | POST | Creates a Confluence page in Atlassian MCP. |
| [Confluence - Get Page](actions/confluence-get-page.md) | GET | Retrieves a Confluence page by ID from Atlassian MCP. |
| [Confluence - List Page Descendants](actions/confluence-list-page-descendants.md) | GET | Retrieves descendant pages for a Confluence page. |
| [Confluence - List Space Pages](actions/confluence-list-space-pages.md) | GET | Retrieves pages from a Confluence space in Atlassian MCP. |
| [Confluence - Search Pages](actions/confluence-search-pages.md) | GET | Searches Confluence content by CQL in Atlassian MCP. |
| [Confluence - Update Page](actions/confluence-update-page.md) | PUT | Updates a Confluence page in Atlassian MCP. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Jira - List Visible Projects](actions/jira-list-visible-projects.md) | GET | Retrieves Jira projects the user can access in Atlassian MCP. |

### Results

| Action | Method | Description |
| --- | --- | --- |
| [Shared Platform - Search](actions/shared-platform-search.md) | GET | Searches Jira and Confluence content in Atlassian MCP. |

### Sites

| Action | Method | Description |
| --- | --- | --- |
| [Shared Platform - List Accessible Resources](actions/shared-platform-list-accessible-resources.md) | GET | Retrieves accessible Atlassian cloud sites from Atlassian MCP. |

### Spaces

| Action | Method | Description |
| --- | --- | --- |
| [Confluence - List Spaces](actions/confluence-list-spaces.md) | GET | Retrieves Confluence spaces from Atlassian MCP. |

### Transitions

| Action | Method | Description |
| --- | --- | --- |
| [Jira - List Issue Transitions](actions/jira-list-issue-transitions.md) | GET | Retrieves available Jira issue transitions from Atlassian MCP. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Jira - Lookup Account ID](actions/jira-lookup-account-id.md) | GET | Finds a Jira account ID by name or email. |
| [Shared Platform - Get Current User](actions/shared-platform-get-current-user.md) | GET | Retrieves current Atlassian user details from Atlassian MCP. |

### Worklogs

| Action | Method | Description |
| --- | --- | --- |
| [Jira - Add Worklog](actions/jira-add-worklog.md) | POST | Adds a worklog to a Jira issue in Atlassian MCP. |

