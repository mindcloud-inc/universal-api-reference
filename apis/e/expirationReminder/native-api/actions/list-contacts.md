# List Contacts with Expiration Reminder

Retrieves contacts from Expiration Reminder.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.expirationreminder.net`
- **Official documentation:** [List Contacts](https://developers.expirationreminder.com/api-reference/contacts-get-all-contacts)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter contacts by email address. |
| `page` | query | `string` | no | Page number to fetch. |
| `sort` | query | `string` | no | Field name to sort by. |
| `sortDirection` | query | `string` | no | Sort direction. Defaults to asc. |
| `term` | query | `string` | no | Filter contacts by a free-text search term. |
