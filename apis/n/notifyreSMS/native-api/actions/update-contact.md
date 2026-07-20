# Update Contact with Notifyre SMS

Updates an existing contact in Notifyre.

## Endpoint

- **Method:** `PUT`
- **Path:** `/addressbook/contacts/:contactId`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Update Contact](https://docs.notifyre.com/api/address-book-contact-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Contact identifier. |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
| `mobileNumber` | body | `string` | no | Contact mobile number. |
