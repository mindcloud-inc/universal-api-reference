# Add Project To Agent Knowledge with Taskade

Adds a project to a Taskade agent knowledge base.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:agentId/knowledge/project`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Add Project To Agent Knowledge](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/agents/add-project-to-agent-knowledge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent ID. |
| `projectId` | body | `string` | yes | The project ID to add to the agent knowledge base. |
