# Get Project with Damstra Forms

Retrieves a project from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Project](https://sammapi.docs.apiary.io/#reference/projects/project-instance/get-a-project)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique id (numeric) or uuid (string) of the project. |
| `show_managed` | query | `boolean` | no | Show/hide the managed attribute. |
