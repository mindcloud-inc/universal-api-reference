# List Opportunities with Close

Retrieves opportunities from Close.

## Endpoint

- **Method:** `GET`
- **Path:** `/opportunity/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [List Opportunities](https://developer.close.com/resources/opportunities/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | query | `string` | no | Filter by Lead ID. |
| `query` | query | `string` | no | Free-text search query. |
| `status_id` | query | `string` | no | Filter by opportunity status ID. |
| `status_type` | query | `string` | no | Filter by status type. |
| `user_id` | query | `string` | no | Filter by owner user ID. |
