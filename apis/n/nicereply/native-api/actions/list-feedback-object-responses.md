# List Feedback Object Responses with Nicereply

Retrieves responses for a feedback object in Nicereply.

## Endpoint

- **Method:** `GET`
- **Path:** `/feedback-objects/:id/responses`
- **Base URL:** `https://api.nicereply.com`
- **Official documentation:** [List Feedback Object Responses](https://cdn.nicereply.com/s/api/latest/reference/feedback-objects/responses/list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Nicereply feedback object ID. |
