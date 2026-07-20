# List Tasks with MILKEE

Retrieves tasks from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/tasks`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [List Tasks](https://apidocs.milkee.ch/api/resources/tasks.html#list-all-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
