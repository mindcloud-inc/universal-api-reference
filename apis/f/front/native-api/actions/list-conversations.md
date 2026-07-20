# List Conversations with Front

Retrieves a list of conversations from Front.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [List Conversations](https://dev.frontapp.com/reference/list-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search query object string for conversation statuses or ticket status filters. |
| `sort_by` | query | `list` | no | Accepted values: `date`. |
| `sort_order` | query | `list` | no | Accepted values: `asc`, `desc`. |
