# Create Datasource with Chatvolt AI

Creates a datasource in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasources`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Datasource](https://docs.chatvolt.ai/api-reference/endpoint/datasources/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | File for multipart/form-data requests. |
| `fileName` | body | `string` | no | Optional name for the uploaded file. If not provided, the original file name will be used. |
| `type` | body | `string` | yes | Type for multipart/form-data requests. |
| `datastoreId` | body | `string` | yes | DatastoreId for multipart/form-data requests. |
| `custom_id` | body | `string` | no | Optional custom ID, useful for multi-tenant configurations to filter data later. |
| `name` | body | `string` | no | Name for application/json requests. |
| `datasourceText` | body | `string` | no | Textual content of the data source (used for `file` and `qa` types when `isUpdateText` is true). |
| `id` | body | `string` | no | Optional ID of the existing datasource for update (upsert). If provided, the corresponding datasource will be updated; otherwise, a new one will be created. |
| `config` | body | `object` | no | Config for application/json requests. |
