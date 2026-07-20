# List Leads with Close

Retrieves leads from Close.

## Endpoint

- **Method:** `GET`
- **Path:** `/lead/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [List Leads](https://developer.close.com/resources/leads/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Free-text search query for leads. |
| `status_id` | query | `string` | no | Filter by lead status ID. |
| `user_id` | query | `string` | no | Filter by owner user ID. |
