# Create Member with Referral Rock

Creates a new member in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/members`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Create Member](https://api.referralrock.com/Help/Api/POST-api-members_shouldSendEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shouldSendEmail` | query | `boolean` | no | Send the program confirmation email to the new member. |
| `programId` | body | `string` | yes | The ID of the referral program to add the member to. |
| `recruiterSourceId` | body | `string` | no | Required when recruiterAssignedId is supplied. |
| `firstName` | body | `string` | yes | — |
| `lastName` | body | `string` | no | — |
| `email` | body | `string` | yes | — |
| `referralCode` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `externalIdentifier` | body | `string` | no | Alternative ID used to link the member to external systems. |
| `dateOfBirth` | body | `date` | no | — |
| `addressLine1` | body | `string` | no | — |
| `addressLine2` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `countrySubdivision` | body | `string` | no | A country subdivision such as a state or province. |
| `country` | body | `string` | no | — |
| `postalCode` | body | `string` | no | — |
| `password` | body | `string` | no | — |
| `disabledFlag` | body | `boolean` | no | Set this when the member should not be enabled for referral programs. |
| `payoutInfo` | body | `object` | no | Optional payout details for the member. |
| `payoutType` | body | `string` | no | — |
| `useDefaultValues` | body | `boolean` | no | — |
| `email` | body | `string` | no | — |
| `customOption1Name` | body | `string` | no | — |
| `customOption1Value` | body | `string` | no | — |
| `customText1Name` | body | `string` | no | — |
| `customText1Value` | body | `string` | no | — |
| `customText2Name` | body | `string` | no | — |
| `customText2Value` | body | `string` | no | — |
| `customOverrideURL` | body | `string` | no | — |
| `recruiterAssignedId` | body | `string` | no | — |
