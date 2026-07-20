# List Messages with Sendblue

Retrieves a list of messages from Sendblue.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/messages`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [List Messages](https://docs.sendblue.com/api/resources/messages/methods/list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_email` | query | `string` | no | Filter by account email. |
| `created_at_gte` | query | `date` | no | Only include messages created at or after this ISO 8601 timestamp. |
| `created_at_lte` | query | `date` | no | Only include messages created at or before this ISO 8601 timestamp. |
| `from_number` | query | `string` | no | Filter by sending number. |
| `group_id` | query | `string` | no | Filter by group ID. |
| `is_outbound` | query | `boolean` | no | Filter outbound vs inbound messages. |
| `message_type` | query | `string` | no | Filter by message type. |
| `number` | query | `string` | no | Filter by recipient number. |
| `sendblue_number` | query | `string` | no | Filter by Sendblue number. |
| `sent_at_gte` | query | `date` | no | Only include messages sent at or after this ISO 8601 timestamp. |
| `sent_at_lte` | query | `date` | no | Only include messages sent at or before this ISO 8601 timestamp. |
| `service` | query | `string` | no | Filter by service. |
| `status` | query | `string` | no | Filter by delivery status. |
| `to_number` | query | `string` | no | Filter by to-number. |
| `updated_at_gte` | query | `date` | no | Only include messages updated at or after this ISO 8601 timestamp. |
| `updated_at_lte` | query | `date` | no | Only include messages updated at or before this ISO 8601 timestamp. |
| `worker_id` | query | `string` | no | Filter by worker ID. |
