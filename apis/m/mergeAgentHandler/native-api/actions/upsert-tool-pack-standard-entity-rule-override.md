# Upsert Tool Pack Standard Entity Rule Override with Merge Agent Handler

Creates or updates a tool pack standard entity rule override in Merge Agent Handler.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tool-packs/:tool_pack_id/standard-entity-rules/:entity_type/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Upsert Tool Pack Standard Entity Rule Override](https://docs.merge.dev/merge-agent-handler/agent-handler/standard-entity-rules/upsert-standard-entity-rule-override-tool-pack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | no | Entity type for the standard entity rule. |
| `tool_pack_id` | path | `string` | no | ID of the tool pack. |
