# List Drawing Annotations with Damstra Forms

Retrieves drawing annotations from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawing_annotations`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Drawing Annotations](https://sammapi.docs.apiary.io/#reference/drawing-annotations/drawing-annotations-collection/get-a-list-of-drawing-annotations)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Only return results belonging to the project with the specified id. |
| `updated_from` | query | `string` | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. |
