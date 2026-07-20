# Get Comment with Nozbe Personal

Retrieves a comment from Nozbe Personal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Get Comment](https://api4.nozbe.com/v1/api#/comments/getCommentById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Comment ID to retrieve. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
