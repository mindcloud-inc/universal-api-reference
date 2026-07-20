# List Contacts with Systeme.io

Retrieves the collection of contacts from Systeme.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/contacts`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [List Contacts](https://developer.systeme.io/reference/api_contacts_get_collection-1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter by exact email. |
| `tags` | query | `string` | no | Filter by tag IDs separated by commas. |
| `bounced` | query | `boolean` | no | Filter by contact bounced state. |
| `unsubscribed` | query | `boolean` | no | Filter by contact unsubscribed state. |
| `needsConfirmation` | query | `boolean` | no | Filter by contact needs confirmation state. |
| `registeredBefore` | query | `date` | no | Filter contacts registered before a date-time. |
| `registeredAfter` | query | `date` | no | Filter contacts registered after a date-time. |
