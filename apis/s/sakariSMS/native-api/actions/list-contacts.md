# List Contacts with Sakari SMS

Retrieves account contacts from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/contacts`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Contacts](https://developer.sakari.io/api-reference/contacts/fetch-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastName` | query | `string` | no | Filter by last name or part of |
| `mobile` | query | `string` | no | Filter by mobile or part of |
| `email` | query | `string` | no | Filter by email or part of |
| `tags` | query | `string` | no | Filter by tag(s) |
| `tags` | query | `string` | no | Filter by tag(s) |
