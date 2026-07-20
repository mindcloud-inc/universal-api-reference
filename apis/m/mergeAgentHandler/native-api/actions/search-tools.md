# Search Tools with Merge Agent Handler

Finds tools in Merge Agent Handler by user intent.

## Endpoint

- **Method:** `POST`
- **Path:** `/tool-packs/:tool_pack_id/registered-users/:registered_user_id/search/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Search Tools](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-search/search-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registered_user_id` | path | `string` | no | ID of the registered user. |
| `tool_pack_id` | path | `string` | no | ID of the tool pack. |
