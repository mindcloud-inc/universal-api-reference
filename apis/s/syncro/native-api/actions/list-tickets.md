# List Tickets with Syncro

Retrieves a list of tickets from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Tickets](https://api-docs.syncromsp.com/#/Ticket/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | query | `number` | no |
| `contact_id` | query | `number` | no |
| `number` | query | `string` | no |
| `resolved_after` | query | `date` | no |
| `created_after` | query | `date` | no |
| `since_updated_at` | query | `date` | no |
| `status` | query | `string` | no |
| `query` | query | `string` | no |
| `user_id` | query | `number` | no |
| `mine` | query | `boolean` | no |
| `ticket_search_id` | query | `number` | no |
| `page` | query | `number` | no |
| `comment_format` | query | `string` | no |
| `all_comments` | query | `boolean` | no |
