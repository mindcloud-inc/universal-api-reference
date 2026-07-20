# List Projects with Damstra Forms

Retrieves projects from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Projects](https://sammapi.docs.apiary.io/#reference/projects/project-collection/get-a-list-of-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `string` | no | Active state (true = Active projects, false = Inactive projects, all = All projects). Accepted values: `0`, `1`, `2`. |
| `updated_from` | query | `string` | no | Only return projects updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |
| `show_managed` | query | `boolean` | no | Show/hide the managed attribute. |
