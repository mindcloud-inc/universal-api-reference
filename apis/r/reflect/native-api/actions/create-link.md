# Create Link with Reflect

Creates a new link in a Reflect graph.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphs/:graphId/links`
- **Base URL:** `https://reflect.app/api`
- **Official documentation:** [Create Link](https://openpm.ai/packages/reflect#/graphs/{graphId}/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `list<string>` | yes | Your graph identifier |
| `url` | body | `string` | yes | — |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `highlights[]` | body | `array<string>` | no | List of highlighted text snippets |
