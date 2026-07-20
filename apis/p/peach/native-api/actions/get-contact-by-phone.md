# Get Contact By Phone with Peach

Retrieves a contact from Peach by phone number.

## Endpoint

- **Method:** `POST`
- **Path:** `/getContact`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Get Contact By Phone](https://peach-organization.gitbook.io/peach/api-reference/contacts/get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | body | `string` | yes | The phone number to look up. |
