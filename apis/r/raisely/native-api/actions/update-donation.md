# Update Donation with Raisely

Updates an existing donation in Raisely.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/donations/:uuid`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Update Donation](https://developers.raisely.com/reference/patchdonation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The `uuid` of the record |
| `data` | body | `object` | no | — |
| `anonymous` | body | `boolean` | no | Does the donor wish to be anonymous Examples: `true`, `false` |
| `email` | body | `string` | no | Email address of the donor Example: `null` |
| `firstName` | body | `string` | no | (deprecated, use preferredName) Example: `null` |
| `fullName` | body | `string` | no | The full name of the person Example: `Leila Norma Eulalia Josefa Magistrado de Lima` |
| `lastName` | body | `string` | no | Last name of the donor Example: `null` |
| `thankyou` | body | `object` | no | — |
| `message` | body | `string` | no | Message to the donor from the fundraiser Example: `Thank you for your donation!` |
| `isPrivate` | body | `boolean` | no | Does the fundraiser want the message to be private Examples: `true`, `false` |
| `preferredName` | body | `string` | no | The name that the person prefers to be called Example: `Norma` |
| `private` | body | `object` | no | Private values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `public` | body | `object` | no | Public values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `currency_symbol` | body | `string` | no | Currency symbol |
| `donation_amount` | body | `string` | no | Amount donated in dollars |
| `fee` | body | `string` | no | The fee paid on the donation in dollars |
| `fixed_amount` | body | `string` | no | — |
| `fixed_description` | body | `string` | no | — |
| `photo_url` | body | `string` | no | Donor photo url |
