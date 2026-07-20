# Update Contact with Streak

Updates an existing contact in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/contacts/:contactKey`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Update Contact](https://streak.readme.io/reference/update-a-contact-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactKey` | path | `string` | yes | Contact key. |
| `teamKey` | body | `string` | no | Streak team key. |
| `emailAddresses` | body | `string<string>` | no | Email addresses to associate with the contact. Send multiple values as a array. |
| `givenName` | body | `string` | no | First name. |
| `familyName` | body | `string` | no | Last name. |
| `title` | body | `string` | no | Contact title or description. |
| `other` | body | `string` | no | Notes or other uncategorized information. |
| `addresses` | body | `string<string>` | no | Addresses to associate with the contact. Send multiple values as a array. |
| `phoneNumbers` | body | `string<string>` | no | Phone numbers to associate with the contact. Send multiple values as a array. |
| `twitterHandle` | body | `string` | no | Twitter handle. |
| `facebookHandle` | body | `string` | no | Facebook handle. |
| `linkedinHandle` | body | `string` | no | LinkedIn handle. |
| `photoUrl` | body | `string` | no | Photo URL. |
