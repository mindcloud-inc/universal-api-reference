# Update Contact with Growby

Updates an existing contact in Growby.

## Endpoint

- **Method:** `PUT`
- **Path:** `/devapi/contact/:id`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Update Contact](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Growby contact id to update. |
| `FirstName` | body | `string` | yes | Updated first name. Required by Growby. |
| `NationalNumber` | body | `string` | yes | Updated phone number without country code. Required by Growby. |
| `CountryCode` | body | `number` | yes | Updated numeric country code. Required by Growby. |
| `LastName` | body | `string` | no | Updated last name. |
| `EmailId` | body | `string` | no | Updated email address. |
| `Source` | body | `string` | no | Updated lead source or origin label. |
