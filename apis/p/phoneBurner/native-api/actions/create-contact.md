# Create Contact with PhoneBurner

Creates a new contact in PhoneBurner.

## Endpoint

- **Method:** `POST`
- **Path:** `rest/1/contacts`
- **Base URL:** `https://www.phoneburner.com/`
- **Official documentation:** [Create Contact](https://www.phoneburner.com/developer/route_list#contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Primary email address for the contact. |
| `first_name` | body | `string` | no | First name of the contact. |
| `last_name` | body | `string` | no | Last name of the contact. |
| `notes` | body | `string` | no | Notes to store on the contact. |
| `phone` | body | `string` | no | Primary phone number for the contact. |
