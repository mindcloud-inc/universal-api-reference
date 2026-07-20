# Sync Contacts with Spoki

Creates a contact or updates an existing one using the provided contact data.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/sync/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Sync Contacts](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | The contact phone number. |
| `first_name` | body | `string` | no | The contact first name. |
| `last_name` | body | `string` | no | The contact last name. |
| `email` | body | `string` | no | The contact email address. |
| `language` | body | `string` | no | The contact language code. |
| `custom_fields` | body | `object` | no | Custom fields keyed by Spoki field code. |
