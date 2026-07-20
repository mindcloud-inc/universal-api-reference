# List Workflows with Skyvern

Retrieves workflows and their latest versions from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workflows`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [List Workflows](https://www.skyvern.com/docs/api-reference/workflows/get-workflows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `string` | no | Filter workflows by folder ID. |
| `only_saved_tasks` | query | `boolean` | no | — |
| `only_templates` | query | `boolean` | no | — |
| `only_workflows` | query | `boolean` | no | — |
| `search_key` | query | `string` | no | Case-insensitive substring search across workflow title, folder name, and parameter metadata. |
| `status[]` | query | `array<string>` | no | — |
| `template` | query | `boolean` | no | — |
