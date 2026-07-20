# <img src="https://images.mindcloud.co/apps/icons/release0_1774886932244.png" alt="Release0 logo" width="28" height="28"> Release0: Universal API

Build, publish, and analyze conversational agents and interactive forms for lead qualification, support, onboarding, and AI-driven chats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/release0/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://release0.com
- **Vendor API docs:** https://docs.release0.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Release0. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Release0. |
| [Get Published Agent](actions/get-published-agent.md) | GET | Retrieves the published version of a Release0 agent. |
| [Import Agent](actions/import-agent.md) | POST | Imports an agent into Release0. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents in a Release0 workspace. |
| [List Linked Agents](actions/list-linked-agents.md) | GET | Retrieves agents linked to a Release0 agent. |
| [Publish Agent](actions/publish-agent.md) | PUT | Publishes an agent for public access in Release0. |
| [Unpublish Agent](actions/unpublish-agent.md) | PUT | Unpublishes an agent from public access in Release0. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an agent in Release0. |

### Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Analytics Stats](actions/get-agent-analytics-stats.md) | GET | Retrieves analytics stats for a Release0 agent. |

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Collaborators](actions/list-agent-collaborators.md) | GET | Retrieves collaborators for a Release0 agent. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a custom domain in Release0. |
| [List Domains](actions/list-domains.md) | GET | Retrieves custom domains from a Release0 workspace. |
| [Verify Domain](actions/verify-domain.md) | GET | Checks whether a custom domain is verified in Release0. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Members](actions/list-workspace-members.md) | GET | Retrieves members of a Release0 workspace. |

### Result

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Results](actions/list-agent-results.md) | GET | Retrieves results for a Release0 agent. |

### Result Log

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Result Logs](actions/list-agent-result-logs.md) | GET | Retrieves execution logs for a Release0 agent result. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Release0. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Release0. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from a Release0 workspace. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Check Workspace Slug](actions/check-workspace-slug.md) | GET | Checks whether a workspace slug is available in Release0. |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Release0. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Release0. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces the current user can access in Release0. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates a workspace in Release0. |

