# Upsert User with Raisely

Finds a user in Raisely, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/upsert`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Upsert User](https://developers.raisely.com/reference/postusersupsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | query | `string` | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
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
| `state` | body | `string` | no | The state/province of the user Examples: `Victoria`, `New York`, `British Columbia` |
| `suburb` | body | `string` | no | The suburb/city of the user Examples: `Melbourne`, `Albany`, `Vancouver` |
| `swiftAidAuthExpiry` | body | `string` | no | Date of expiry of donor authorisation for SwiftAid |
| `tags[]` | body | `array<string>` | no | Tag UUIDs or paths to assign to the user |
| `interaction` | body | `object` | no | The interaction to create assigned to this user |
| `categoryUuid` | body | `string` | no | The category UUID of the interaction to create |
| `detail` | body | `object` | yes | Additional details relating to this Raisely interaction |
| `comment` | body | `string` | no | — |
| `pinned` | body | `boolean` | no | — |
| `private` | query | `object` | no | — |
| `public` | body | `object` | no | — |
| `readOnly` | body | `boolean` | no | — |
