# List Activities with Close

Retrieves activities from Close.

## Endpoint

- **Method:** `GET`
- **Path:** `/activity/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [List Activities](https://developer.close.com/resources/activities/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_type` | query | `string` | no | Filter by activity type. |
| `contact_id` | query | `string` | no | Filter by contact ID. |
| `lead_id` | query | `string` | no | Filter by Lead ID. |
| `user_id` | query | `string` | no | Filter by user ID. |
