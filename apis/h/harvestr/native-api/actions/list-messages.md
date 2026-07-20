# List Messages with Harvestr.io

## Endpoint

- **Method:** `GET`
- **Path:** `/message`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [List Messages](https://developers.harvestr.io/api/list-messages/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_before` | query | `date` | no | Filter items created before this date (ISO 8601 format) |
| `created_after` | query | `date` | no | Filter items created after this date (ISO 8601 format) |
| `updated_before` | query | `date` | no | Filter items updated before this date (ISO 8601 format) |
| `updated_after` | query | `date` | no | Filter items updated after this date (ISO 8601 format) |
| `channel` | query | `string` | no | Filter messages by channel |
| `requesterId` | query | `string` | no | Filter messages by requester ID |
| `hasFeedback` | query | `boolean` | no | Filter messages by whether they have feedback linked or not |
| `customInboxId` | query | `string` | no | Filter messages by custom inbox ID |
