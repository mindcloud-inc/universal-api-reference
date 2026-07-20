# List Trees with Woztell

Retrieves trees from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [List Trees](https://doc.woztell.com/open-api-reference/#query-apiViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include first, after, before, treeIds, search, and sortBy. |
