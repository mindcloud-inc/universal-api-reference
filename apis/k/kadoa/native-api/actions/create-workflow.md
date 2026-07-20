# Create Workflow with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/workflows/`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Create Workflow](https://docs.kadoa.com/api-reference/workflows/create-a-new-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls` | body | `list<string>` | yes | JSON array of URLs to extract from |
| `entity` | body | `string` | yes | Entity type to extract |
| `fields` | body | `list<object>` | yes | JSON array of field definitions |
| `name` | body | `string` | no | Workflow name |
| `description` | body | `string` | no | Workflow description |
| `navigationMode` | body | `string` | no | Navigation mode: single-page, paginated-page, page-and-detail, agentic-navigation, all-pages |
| `limit` | body | `number` | no | Max items to extract |
| `maxPages` | body | `number` | no | Max pages to process |
