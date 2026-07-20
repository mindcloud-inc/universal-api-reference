# Create Contact with Notifyre SMS

Creates a new contact in Notifyre.

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbook/contacts`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Create Contact](https://docs.notifyre.com/api/address-book-contact-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
| `mobileNumber` | body | `string` | yes | Contact mobile number. |
