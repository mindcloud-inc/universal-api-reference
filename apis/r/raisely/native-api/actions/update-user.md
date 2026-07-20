# Update User with Raisely

Updates an existing user in Raisely.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:uuid`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Update User](https://developers.raisely.com/reference/patchuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The `uuid` of the record |
| `data` | body | `object` | no | — |
| `address1` | body | `string` | no | Line 1 of an address Example: `31 Sunset Boulevard` |
| `address2` | body | `string` | no | Line 2 of an address Example: `Unit 31b` |
| `adminSettings` | body | `object` | no | Object containing settings for admin users |
| `country` | body | `string` | no | The country of the user Examples: `AU`, `GB`, `US` |
| `email` | body | `string` | no | The user's email address. Raisely uses this as a unique identifier and will deduplicate on email. Example: `harveymilk@example.com` |
| `firstName` | body | `string` | no | The first name of the user Example: `Leila` |
| `fullName` | body | `string` | no | The full name of the user Example: `Leila Norma de Lima` |
| `isSamlLogin` | body | `boolean` | no | Will be true if this user logs in via organisation SAML login Examples: `true`, `false` |
| `language` | body | `string` | no | The language the user last interacted in |
| `lastName` | body | `string` | no | The last name of the user Example: `de Lima` |
| `phoneNumber` | body | `string` | no | Phone number of the user Example: `+1 123-456-7890` |
| `photoUrl` | body | `string` | no | URL of the user's photo Example: `https://raisely-images.imgix.net/www/uploads/t-03-arl-8-es-uhhqua-4-pr-f-4865431-df-58-512-png-08e3f5.png` |
| `postcode` | body | `string` | no | Postal code of the user Examples: `AAA BBBB`, `0000`, `AAA BBB` |
| `preferredName` | body | `string` | no | The name that the user prefers to be called Example: `Norma` |
| `private` | query | `object` | no | Private values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `public` | body | `object` | no | Public values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `state` | body | `string` | no | The state/province of the user Examples: `Victoria`, `New York`, `British Columbia` |
| `suburb` | body | `string` | no | The suburb/city of the user Examples: `Melbourne`, `Albany`, `Vancouver` |
| `swiftAidAuthExpiry` | body | `string` | no | Date of expiry of donor authorisation for SwiftAid |
| `overwriteCustomFields` | body | `boolean` | no | If passed, replace the existing `public` and `private` values on the record with the values provided with this payload |
