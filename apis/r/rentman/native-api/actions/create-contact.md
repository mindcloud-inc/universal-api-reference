# Create Contact with Rentman

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [Create Contact](https://api.rentman.net/#operation/createContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Contact name. |
| `type` | body | `string` | no | Contact type: private or company. |
| `email_1` | body | `string` | no | Primary email address. |
| `phone_1` | body | `string` | no | Primary phone number. |
| `mailing_city` | body | `string` | no | Mailing city. |
