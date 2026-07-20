# Create Donation with Raisely

Creates a new donation in Raisely.

## Endpoint

- **Method:** `POST`
- **Path:** `/donations`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Create Donation](https://developers.raisely.com/reference/postdonations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | — |
| `address1` | body | `string` | no | Line 1 of an address Example: `31 Sunset Boulevard` |
| `address2` | body | `string` | no | Line 2 of an address Example: `Unit 31b` |
| `anonymous` | body | `boolean` | no | Does the donor wish to be anonymous Examples: `true`, `false` |
| `campaignUuid` | body | `string` | no | Unique identifier for the record Example: `aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa` |
| `card` | body | `string` | no | ID of the payment method used (from the payment gateway) Example: `card_aabbccddeeffaabbccddeeff` |
| `country` | body | `string` | no | Examples: `AU`, `GB`, `US` |
| `currency` | body | `string` | yes | 3 letter currency code Examples: `AUD`, `USD` |
| `customer` | body | `string` | no | The customer ID (assigned by the payment gateway) |
| `date` | body | `string` | no | The date and time (in ISO8601 format) the donation was received by the organisation (only for OFFLINE donations) Example: `2020-12-03T06:52:46.330Z` |
| `email` | body | `string` | yes | Email address of the donor Example: `harveymilk@example.com` |
| `firstName` | body | `string` | no | The first name of the person Example: `Leila` |
| `forRegistration` | body | `string` | no | Not null values indicate this transaction has been set aside to pay for an upcoming registration Examples: `true`, `null` |
| `fullName` | body | `string` | no | The full name of the person Example: `Leila Norma Eulalia Josefa Magistrado de Lima` |
| `gatewayVersion` | body | `string` | no | Gateway Version of donation method, if any |
| `items` | body | `object<object>` | no | — |
| `amount` | body | `number` | no | The amount spent on the item in the currency of the donation |
| `amountRefunded` | body | `number` | no | The total amount refunded in cents for this line item, in the donation currency. |
| `attendance` | body | `string` | no | Whether the donation item (ticket) has been checked in |
| `description` | body | `string` | no | Description of the item |
| `includeInTotals` | body | `boolean` | no | If false, the amount is not included in receipts as part of the total donation |
| `parentBundleItemDescription` | body | `string` | no | The ticket's parent bundle description |
| `quantity` | body | `number` | no | If multiple of the item, the number of items claimed |
| `lastName` | body | `string` | no | The last name of the person Example: `de Lima` |
| `message` | body | `string` | no | Message from the donor Example: `Glad to help out with the fundraising!` |
| `method` | body | `string` | yes | The payment gateway used Examples: `CREDIT_CARD`, `PAYPAL`, `APPLE_PAY`, `OFFLINE`, `CUSTOM`, `STRIPE_INTENT`, `FACEBOOK` |
| `methodType` | body | `string` | no | The type of payment method used, to distinguish between card, direct debit and digital wallet payments. Examples: `APPLE_PAY`, `CARD`, `GOOGLE_PAY`, `BROWSER_PAY` |
| `mode` | body | `string` | no | LIVE or TEST Examples: `LIVE`, `TEST` |
| `phoneNumber` | body | `string` | no | Phone number of the donor Example: `+1 123-456-7890` |
| `postcode` | body | `string` | no | Postal code of the donor Examples: `AAA BBBB`, `0000`, `AAA BBB` |
| `preferredName` | body | `string` | no | The name that the person prefers to be called Example: `Norma` |
| `private` | query | `object` | no | Private values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `profileUuid` | body | `string` | no | Unique identifier for the record Example: `aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa` |
| `public` | body | `object` | no | Public values for this record Example: `{   "fieldA": "one",   "fieldB": "yes" }` |
| `state` | body | `string` | no | — |
| `suburb` | body | `string` | no | — |
| `swiftAidStatus` | body | `string` | no | Status of donation on SwiftAid Examples: `OK`, `FAILED`, `PENDING`, `DELETING`, `DELETED` |
| `token` | body | `string` | no | The payment token from the gateway Example: `tok_aaaaaaaaaaaaaaaaaaaaaaaa` |
| `type` | body | `string` | yes | ONLINE or OFFLINE Examples: `ONLINE`, `OFFLINE` |
