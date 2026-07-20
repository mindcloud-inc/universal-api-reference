# Get Agent Workflow with Mona AI

Retrieves a workflow for a Mona AI agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/getAgentWorkflow`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Agent Workflow](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | Mona agent identifier that owns the workflow. |
| `permission` | body | `string` | yes | Mona permission string required by this workflow lookup endpoint. |
| `workflowId` | body | `string` | yes | Mona workflow identifier to retrieve. |
