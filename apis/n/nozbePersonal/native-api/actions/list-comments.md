# List Comments with Nozbe Personal

Retrieves accessible comments from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Comments](https://api4.nozbe.com/v1/api#/comments/getComments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | no | Filter comments by task. |
| `sortBy` | query | `string` | no | Comma-separated sort expression. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
