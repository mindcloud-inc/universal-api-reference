# List Contacts with Evenium

Retrieves contacts from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Contacts](https://static.evenium.com/api-docs/organizer/index-json.html#_get_all_contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | query | `string` | no | Only retrieve contacts whose company matches. |
| `email` | query | `string` | no | Only retrieve contacts whose email matches. |
| `firstName` | query | `string` | no | Only retrieve contacts whose first name matches. |
| `lastName` | query | `string` | no | Only retrieve contacts whose last name matches. |
| `since` | query | `string` | no | Only retrieve contacts updated after this date. |
