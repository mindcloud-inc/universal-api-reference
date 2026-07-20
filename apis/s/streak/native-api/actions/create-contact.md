# Create Contact with Streak

Creates a new contact in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/teams/:teamKey/contacts/`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Create Contact](https://streak.readme.io/reference/create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamKey` | path | `string` | yes | Team key. |
| `emailAddresses` | body | `string<string>` | yes | Email addresses to associate with the contact. Send multiple values as a array. |
| `getIfExisting` | query | `boolean` | no | If true, return an existing contact when the email already exists. |
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
