# Create Contact with Autotask

## Endpoint

- **Method:** `POST`
- **Path:** `/Companies/:parentId/Contacts`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Create Contact](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | path | `number` | yes | Company associated with the contact. Autotask requires this company ID in the contact child-resource path. |
| `firstName` | body | `string` | yes | Maximum length: 20. |
| `lastName` | body | `string` | yes | Maximum length: 20. |
| `isActive` | body | `number` | yes | — |
| `emailAddress` | body | `string` | no | Maximum length: 254. |
| `phone` | body | `string` | no | Maximum length: 25. |
| `mobilePhone` | body | `string` | no | Maximum length: 25. |
| `title` | body | `string` | no | Maximum length: 50. |
| `primaryContact` | body | `boolean` | no | Making this contact primary clears the previous primary contact for the company. |
| `billingContact` | body | `boolean` | no | — |
| `receivesEmailNotifications` | body | `boolean` | no | — |
| `additionalAddressInformation` | body | `string` | no | Maximum length: 100. |
| `addressLine` | body | `string` | no | Maximum length: 128. |
| `addressLine1` | body | `string` | no | Maximum length: 128. |
| `city` | body | `string` | no | Maximum length: 32. |
| `state` | body | `string` | no | Maximum length: 40. |
| `zipCode` | body | `string` | no | Maximum length: 16. |
| `countryID` | body | `number` | no | — |
| `companylocationID` | body | `number` | no | — |
| `alternatePhone` | body | `string` | no | Maximum length: 32. |
| `extension` | body | `string` | no | Maximum length: 10. |
| `faxNumber` | body | `string` | no | Maximum length: 25. |
| `emailAddress2` | body | `string` | no | Maximum length: 254. |
| `emailAddress3` | body | `string` | no | Maximum length: 254. |
| `externalID` | body | `string` | no | Maximum length: 50. |
| `facebookUrl` | body | `string` | no | Maximum length: 200. |
| `linkedInUrl` | body | `string` | no | Maximum length: 200. |
| `twitterUrl` | body | `string` | no | Maximum length: 200. |
| `middleInitial` | body | `string` | no | Maximum length: 50. |
| `namePrefix` | body | `number` | no | — |
| `nameSuffix` | body | `number` | no | — |
| `note` | body | `string` | no | API-only note displayed in customized Contact Insight views. Maximum length: 50. |
| `roomNumber` | body | `string` | no | Maximum length: 50. |
| `isOptedOutFromBulkEmail` | body | `boolean` | no | — |
| `userDefinedFields[]` | body | `array<object>` | no | Optional contact user-defined fields. |
| `userDefinedFields[].name` | body | `string` | no | — |
| `userDefinedFields[].value` | body | `string` | no | — |
