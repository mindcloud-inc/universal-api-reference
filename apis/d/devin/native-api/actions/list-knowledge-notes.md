# List Knowledge Notes with Devin

Retrieves a list of knowledge notes from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/knowledge/notes`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [List Knowledge Notes](https://docs.devin.ai/api-reference/v3/notes/organizations-knowledge-notes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
