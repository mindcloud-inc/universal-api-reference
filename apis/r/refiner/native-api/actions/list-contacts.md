# List Contacts with Refiner

Retrieves contacts from your Refiner account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [List Contacts](https://refiner.io/docs/api/#get-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search contact email, ID, or name. |
| `form_uuid` | query | `string` | no | Only include contacts linked to a specific survey. |
| `segment_uuid` | query | `string` | no | Only include contacts matching a specific segment. |
| `order_by` | query | `string` | no | Sort contacts by first_seen_at, last_seen_at, or last_form_submission_at. |
| `page_cursor` | query | `string` | no | Cursor for the next contacts page. |
