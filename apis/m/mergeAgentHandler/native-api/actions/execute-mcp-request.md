# Execute MCP Request with Merge Agent Handler

Executes an MCP request in Merge Agent Handler.

## Endpoint

- **Method:** `POST`
- **Path:** `/tool-packs/:tool_pack_id/registered-users/:registered_user_id/mcp/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Execute MCP Request](https://docs.merge.dev/merge-agent-handler/agent-handler/mcp/endpoint-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registered_user_id` | path | `string` | no | ID of the registered user. |
| `tool_pack_id` | path | `string` | no | ID of the tool pack. |
