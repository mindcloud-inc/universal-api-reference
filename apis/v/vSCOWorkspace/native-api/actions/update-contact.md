# Update Contact with VSCO Workspace

Updates an existing contact in VSCO Workspace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/address-book/:id`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Update Contact](https://workspace.vsco.co/api/#operation/updateResourceAddressBook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `kind` | body | `string` | yes | — |
| `anniversary` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `bestDayToCall` | body | `string` | no | — |
| `bestTimeToCall` | body | `string` | no | — |
| `birthdate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `brandId` | body | `object` | no | — |
| `cellPhone` | body | `object` | no | — |
| `companyName` | body | `string` | no | — |
| `contactPreference` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `fax` | body | `object` | no | — |
| `firstName` | body | `string` | no | — |
| `gender` | body | `string` | no | — |
| `homePhone` | body | `object` | no | — |
| `jobTitle` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `maidenName` | body | `string` | no | — |
| `mailingAddress` | body | `object` | no | Represents an address. |
| `previousClient` | body | `boolean` | no | — |
| `privacyOptIn` | body | `boolean` | no | Contact has Opted-In to Marketing and Processing |
| `requireStrictPrivacy` | body | `boolean` | no | Require Strict Privacy (e.g. subject to Europe's GDPR) |
| `salutation` | body | `string` | no | — |
| `schoolGradYear` | body | `number` | no | — |
| `schoolName` | body | `string` | no | — |
| `sport` | body | `string` | no | — |
| `startingCost` | body | `object` | no | — |
| `startingRevenue` | body | `object` | no | — |
| `teamName` | body | `string` | no | — |
| `teamPosition` | body | `string` | no | — |
| `vendorRoleId` | body | `string` | no | This is a vendor and defines the default job role does this contact have when added to a job. |
| `workPhone` | body | `object` | no | — |
| `address` | body | `object` | no | Represents an address. |
| `chatAccount1` | body | `object` | no | — |
| `chatAccount2` | body | `object` | no | — |
| `chatAccount3` | body | `object` | no | — |
| `customFields[]` | body | `array<object>` | no | — |
| `facebookUsername` | body | `string` | no | — |
| `notes[]` | body | `array<object>` | no | A list of notes attached to this contact. This will only be returned in a get of a specific contact and not in the list response. |
| `pinned` | body | `boolean` | no | — |
| `secondaryEmail` | body | `string` | no | — |
| `totalCost` | body | `object` | no | — |
| `totalRevenue` | body | `object` | no | — |
| `twitterUsername` | body | `string` | no | — |
| `url` | body | `string` | no | — |
| `accountNumber` | body | `string` | no | — |
| `phone` | body | `object` | no | — |
| `primaryContactFirstName` | body | `string` | no | — |
| `primaryContactLastName` | body | `string` | no | — |
| `tollFree` | body | `object` | no | — |
