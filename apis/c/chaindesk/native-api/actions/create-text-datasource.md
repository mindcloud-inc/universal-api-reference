# Create Text Datasource with Chaindesk

Creates a text datasource in Chaindesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasources`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [Create Text Datasource](https://docs.chaindesk.ai/api-reference/endpoint/datasources/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datastoreId` | body | `string` | yes |
| `text` | body | `string` | yes |
