# Delete Tool Pack Custom Regex Rule with Merge Agent Handler

Deletes a tool pack custom regex rule from Merge Agent Handler.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tool-packs/:tool_pack_id/custom-regex-rules/:rule_id/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Delete Tool Pack Custom Regex Rule](https://docs.merge.dev/merge-agent-handler/agent-handler/custom-regex-rules/delete-custom-regex-rule-tool-pack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rule_id` | path | `string` | no | ID of the custom regex rule. |
| `tool_pack_id` | path | `string` | no | ID of the tool pack. |
