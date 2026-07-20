# List Drawings with Damstra Forms

Retrieves drawings from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Drawings](https://sammapi.docs.apiary.io/#reference/drawings/drawings-collection/get-a-list-of-drawings)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Only return results belonging to the project with the specified id. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |
