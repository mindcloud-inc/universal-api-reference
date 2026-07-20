# Bulk Upsert Tool Pack Tool Description Overrides with Merge Agent Handler

Upserts or deletes tool pack description overrides in Merge Agent Handler.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tool-packs/:tool_pack_id/tool-description-overrides/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Bulk Upsert Tool Pack Tool Description Overrides](https://docs.merge.dev/merge-agent-handler/agent-handler/tool-description-overrides/bulk-upsert-delete-tool-pack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tool_pack_id` | path | `string` | no | ID of the tool pack. |
