# Get Contact By Email with Peach

Retrieves a contact from Peach by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/getContact`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Get Contact By Email](https://peach-organization.gitbook.io/peach/api-reference/contacts/get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to look up. |
