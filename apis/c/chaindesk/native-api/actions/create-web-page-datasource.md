# Create Web Page Datasource with Chaindesk

Creates a web page datasource in Chaindesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasources`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [Create Web Page Datasource](https://docs.chaindesk.ai/api-reference/endpoint/datasources/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datastoreId` | body | `string` | yes |
| `config.source_url` | body | `string` | yes |
