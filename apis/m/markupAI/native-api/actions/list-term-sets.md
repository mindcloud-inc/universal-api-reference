# List Term Sets with Markup AI

Retrieves term sets from Markup AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/terminology/term-sets`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [List Term Sets](https://docs.markup.ai/api-reference/terminology/list-term-sets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_term` | query | `string` | no | Optional text used to filter term sets. |
| `domain_ids[]` | query | `array<string>` | no | Optional terminology domain IDs to restrict listed term sets. |
