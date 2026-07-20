# Create Contact with Pipefile

Creates a new contact in Pipefile.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/`
- **Base URL:** `https://api.pipefile.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact name. |
| `email` | body | `string` | no | Primary email address for the contact. |
| `phone` | body | `string` | no | Primary phone number for the contact. |
