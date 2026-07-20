# List Views with Braintrust

Retrieves views from Braintrust.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/view`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [List Views](https://braintrust.dev/docs/api-reference/views/list-views.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_type` | query | `string` | yes | Type of object the view applies to. |
| `object_id` | query | `string` | yes | Id of the object the view applies to. |
