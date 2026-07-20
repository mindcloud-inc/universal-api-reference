# Import Agent with Release0

Imports an agent into Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/import`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Import Agent](https://docs.release0.com/api-reference/agent/import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | The workspace that will receive the imported agent. |
| `agent` | body | `object` | yes | The full agent definition to import. |
