# <img src="https://images.mindcloud.co/apps/icons/cradl-ai_1775674313220.png" alt="Cradl AI logo" width="28" height="28"> Cradl AI: Universal API

Build AI agents to automate internal document workflows with AI-powered document processing and human review.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cradlAI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cradl.ai
- **Vendor API docs:** https://docs.cradl.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Cradl AI. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Cradl AI. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Cradl AI. |
| [List Agents](actions/list-agents.md) | GET | Retrieves all agents from Cradl AI. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Cradl AI. |

### Agent Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent Run](actions/create-agent-run.md) | POST | Creates a new agent run in Cradl AI. |
| [Delete Agent Run](actions/delete-agent-run.md) | DELETE | Deletes an existing agent run from Cradl AI. |
| [Get Agent Run](actions/get-agent-run.md) | GET | Retrieves an agent run from Cradl AI. |
| [List Agent Runs](actions/list-agent-runs.md) | GET | Retrieves all agent runs from Cradl AI. |
| [Update Agent Run](actions/update-agent-run.md) | PUT | Updates an existing agent run in Cradl AI. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Cradl AI. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Cradl AI. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Cradl AI. |
| [List Documents](actions/list-documents.md) | GET | Retrieves all documents from Cradl AI. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Cradl AI. |

### Function

| Action | Method | Description |
| --- | --- | --- |
| [Create Function](actions/create-function.md) | POST | Creates a new function in Cradl AI. |
| [Delete Function](actions/delete-function.md) | DELETE | Deletes an existing function from Cradl AI. |
| [Get Function](actions/get-function.md) | GET | Retrieves a function from Cradl AI. |
| [List Functions](actions/list-functions.md) | GET | Retrieves all functions from Cradl AI. |
| [Update Function](actions/update-function.md) | PUT | Updates an existing function in Cradl AI. |

### Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Hook](actions/create-hook.md) | POST | Creates a new hook in Cradl AI. |
| [Delete Hook](actions/delete-hook.md) | DELETE | Deletes an existing hook from Cradl AI. |
| [Get Hook](actions/get-hook.md) | GET | Retrieves a hook from Cradl AI. |
| [List Hooks](actions/list-hooks.md) | GET | Retrieves all hooks from Cradl AI. |
| [Update Hook](actions/update-hook.md) | PUT | Updates an existing hook in Cradl AI. |

