# Create Referral with Referral Rock

Creates a new referral in Referral Rock from a member referral code.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/referrals`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Create Referral](https://api.referralrock.com/Help/Api/POST-api-referrals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referralCode` | body | `string` | yes | Referral code from the member who introduced the referral. |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phoneNumber` | body | `string` | no | — |
| `preferredContact` | body | `string` | no | Allowed values are email, callMorning, callAfternoon, or callEvening. |
| `externalIdentifier` | body | `string` | no | Unique external ID you can use to reference the referral later. |
| `amount` | body | `number` | no | Passed order amount or total. |
| `companyName` | body | `string` | no | — |
| `note` | body | `string` | no | — |
| `publicNote` | body | `string` | no | — |
| `customOption1Name` | body | `string` | no | — |
| `customOption2Name` | body | `string` | no | — |
| `customText1Name` | body | `string` | no | — |
| `customText2Name` | body | `string` | no | — |
| `customText3Name` | body | `string` | no | — |
| `customOption1Value` | body | `string` | no | — |
| `customOption2Value` | body | `string` | no | — |
| `customText1Value` | body | `string` | no | — |
| `customText2Value` | body | `string` | no | — |
| `customText3Value` | body | `string` | no | — |
| `status` | body | `string` | no | Allowed values are pending, qualified, approved, or denied. |
| `addressLine1` | body | `string` | no | — |
| `addressLine2` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `region` | body | `string` | no | Must be a region name or ISO 3166-2 subdivision code, and can only be supplied if country is also provided. |
| `postalCode` | body | `string` | no | — |
| `country` | body | `string` | no | Referral country name or ISO 3166-2 country code. |
| `recruiterAssignedId` | body | `string` | no | — |
