# List Ticket Comments with Syncro

Retrieves comments for a ticket from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:id/comments`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Ticket Comments](https://api-docs.syncromsp.com/#/Ticket/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro ticket ID. |
| `page` | query | `number` | no | — |
| `per_page` | query | `number` | no | — |
| `comment_format` | query | `string` | no | — |
| `sort_by` | query | `string` | no | — |
| `sort_direction` | query | `string` | no | — |
| `created_after` | query | `date` | no | — |
| `created_before` | query | `date` | no | — |
| `updated_after` | query | `date` | no | — |
| `updated_before` | query | `date` | no | — |
