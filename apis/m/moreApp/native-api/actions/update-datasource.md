# Update Datasource with MoreApp

Updates a datasource in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Datasource](https://docs.moreapp.com/docs/developer-docs/52b1fb0c9b961-update-a-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer ID. |
| `dataSourceId` | path | `string` | yes | Datasource ID. |
| `name` | body | `string` | yes | Datasource name. |
| `urlConfiguration.url` | body | `string` | yes | Source URL for URL-based datasources. |
| `urlConfiguration.updateInterval` | body | `string` | yes | Refresh interval for URL-based datasources. |
