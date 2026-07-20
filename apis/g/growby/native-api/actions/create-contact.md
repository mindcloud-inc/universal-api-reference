# Create Contact with Growby

Creates a new contact in Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/devapi/AddContact`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Create Contact](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FirstName` | body | `string` | yes | Contact first name. Required by Growby. |
| `NationalNumber` | body | `string` | yes | Phone number without the country code. Required by Growby. |
| `CountryCode` | body | `number` | yes | Numeric country code for the contact phone number. Required by Growby. |
| `LastName` | body | `string` | no | Contact last name. |
| `EmailId` | body | `string` | no | Contact email address. |
| `Source` | body | `string` | no | Lead source or origin label for the contact. |
