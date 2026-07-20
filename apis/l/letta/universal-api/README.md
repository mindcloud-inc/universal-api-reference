# <img src="https://images.mindcloud.co/apps/icons/letta-icon_1778269322511.png" alt="Letta logo" width="28" height="28"> Letta: Universal API

Build, manage, and message stateful Letta agents with persistent memory.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/letta/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.letta.com
- **Vendor API docs:** https://docs.letta.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Letta. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Letta. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from Letta. |
| [Retrieve Agent](actions/retrieve-agent.md) | GET | Retrieves an existing agent from Letta. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Letta. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves a list of conversations from Letta. |

### Memory Block

| Action | Method | Description |
| --- | --- | --- |
| [Create Block](actions/create-block.md) | POST | Creates a new block in Letta. |
| [List Agent Memory Blocks](actions/list-agent-memory-blocks.md) | GET | Retrieves core memory blocks for an agent in Letta. |
| [List Blocks](actions/list-blocks.md) | GET | Retrieves a list of blocks from Letta. |
| [Retrieve Agent Memory Block](actions/retrieve-agent-memory-block.md) | GET | Retrieves a core memory block from Letta by label. |
| [Update Agent Memory Block](actions/update-agent-memory-block.md) | PUT | Updates a core memory block in Letta by label. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Agent Message](actions/cancel-agent-message.md) | PUT |  |
| [Create Agent Message](actions/create-agent-message.md) | POST | Processes a user message through an agent in Letta. |
| [Create Agent Message Async](actions/create-agent-message-async.md) | POST | Starts an asynchronous agent message run in Letta. |
| [List Agent Messages](actions/list-agent-messages.md) | GET | Retrieves messages from an agent in Letta. |
| [Reset Agent Messages](actions/reset-agent-messages.md) | PUT | Resets an agent's messages in Letta. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available LLM models from Letta. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [List Runs](actions/list-runs.md) | GET | Retrieves a list of runs from Letta. |
| [Retrieve Run](actions/retrieve-run.md) | GET | Retrieves an existing run from Letta. |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Agent Messages](actions/summarize-agent-messages.md) | POST | Summarizes an agent's conversation history in Letta. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Attach Tool To Agent](actions/attach-tool-to-agent.md) | PUT | Attaches a tool to an agent in Letta. |
| [Create Tool](actions/create-tool.md) | POST | Creates a new tool in Letta. |
| [Detach Tool From Agent](actions/detach-tool-from-agent.md) | PUT | Detaches a tool from an agent in Letta. |
| [List Agent Tools](actions/list-agent-tools.md) | GET | Retrieves tools attached to an agent in Letta. |
| [List Tools](actions/list-tools.md) | GET | Retrieves a list of tools from Letta. |

