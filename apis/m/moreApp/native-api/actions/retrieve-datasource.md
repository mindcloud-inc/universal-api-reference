# Retrieve Datasource with MoreApp

Retrieves a datasource from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Datasource](https://docs.moreapp.com/docs/developer-docs/1d826aa0c516a-retrieve-a-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer ID. |
| `dataSourceId` | path | `string` | yes | Datasource ID. |
