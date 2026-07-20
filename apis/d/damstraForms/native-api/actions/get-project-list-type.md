# Get Project List Type with Damstra Forms

Retrieves a project list type from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/project_list_types/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Project List Type](https://sammapi.docs.apiary.io/#reference/project-list-types/project-list-type-instance/get-a-project-list-type)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique id (numeric) or uuid (string) identifier of the project list type. |
| `show_managed` | query | `boolean` | no | Show/hide the managed attribute. |
