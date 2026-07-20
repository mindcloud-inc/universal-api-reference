# List Prompt Templates with PromptLayer Run Agent

Retrieves prompt templates from PromptLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/prompt-templates`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [List Prompt Templates](https://docs.promptlayer.com/reference/list-prompt-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Case-insensitive partial match on prompt template name. |
| `label` | query | `string` | no | Filter prompt templates by release label. |
| `status` | query | `list` | no | Filter prompt templates by deletion status: active, deleted, or all. Accepted values: `0`, `1`, `2`. |
