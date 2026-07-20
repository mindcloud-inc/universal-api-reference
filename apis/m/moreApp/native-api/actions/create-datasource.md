# Create Datasource with MoreApp

Creates a datasource in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/datasources`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Datasource](https://docs.moreapp.com/docs/developer-docs/5c7a4e7b26a0e-create-a-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer ID. |
| `name` | body | `string` | yes | Datasource name. |
| `urlConfiguration.url` | body | `string` | yes | Source URL for URL-based datasources. |
| `urlConfiguration.updateInterval` | body | `string` | yes | Refresh interval for URL-based datasources. |
