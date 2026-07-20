# List Contacts with Close

Retrieves contacts from Close.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [List Contacts](https://developer.close.com/resources/contacts/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | query | `string` | no | Filter contacts by lead ID. |
| `query` | query | `string` | no | Free-text search query for contacts. |
