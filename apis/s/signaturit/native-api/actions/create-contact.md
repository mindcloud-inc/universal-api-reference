# Create Contact with Signaturit

Creates a new contact in Signaturit.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [Create Contact](https://docs.signaturit.com/api/latest#contacts_post_contact)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email of the new contact. |
| `name` | body | `string` | yes | Name of the new contact. |
