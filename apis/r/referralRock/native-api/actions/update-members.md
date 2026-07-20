# Update Members with Referral Rock

Updates existing members in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/members/update`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Update Members](https://api.referralrock.com/Help/Api/POST-api-members-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no |
| `items[].member.addressLine1` | body | `string` | no |
| `items[].member.addressLine2` | body | `string` | no |
| `items[].member.city` | body | `string` | no |
| `items[].member.country` | body | `string` | no |
| `items[].member.countrySubdivision` | body | `string` | no |
| `items[].member.customOption1Name` | body | `string` | no |
| `items[].member.customOption1Value` | body | `string` | no |
| `items[].member.customOverrideURL` | body | `string` | no |
| `items[].member.customText1Name` | body | `string` | no |
| `items[].member.customText1Value` | body | `string` | no |
| `items[].member.customText2Name` | body | `string` | no |
| `items[].member.customText2Value` | body | `string` | no |
| `items[].member.email` | body | `string` | no |
| `items[].member.externalIdentifier` | body | `string` | no |
| `items[].member.firstName` | body | `string` | no |
| `items[].member.lastName` | body | `string` | no |
| `items[].member.password` | body | `string` | no |
| `items[].member.payoutInfo.email` | body | `string` | no |
| `items[].member.payoutInfo.payoutType` | body | `string` | no |
| `items[].member.phone` | body | `string` | no |
| `items[].member.postalCode` | body | `string` | no |
| `items[].member.recruiterAssignedId` | body | `string` | no |
| `items[].member.referralCode` | body | `string` | no |
| `items[].member.region` | body | `string` | no |
| `items[].query.primaryInfo.memberId` | body | `string` | no |
| `items[].query.primaryInfo.referralCode` | body | `string` | no |
| `items[].query.secondaryInfo.email` | body | `string` | no |
| `items[].query.secondaryInfo.externalIdentifier` | body | `string` | no |
| `items[].query.tertiaryInfo.programId` | body | `string` | no |
| `items[].query.tertiaryInfo.programName` | body | `string` | no |
| `items[].query.tertiaryInfo.programTitle` | body | `string` | no |
| `items[].query` | body | `object` | yes |
| `items[].query.primaryInfo` | body | `object` | no |
| `items[].query.secondaryInfo` | body | `object` | no |
| `items[].query.tertiaryInfo` | body | `object` | no |
| `items[].member` | body | `object` | yes |
| `items[].member.dateOfBirth` | body | `date` | no |
| `items[].member.disabledFlag` | body | `boolean` | no |
| `items[].member.payoutInfo` | body | `object` | no |
| `items[].member.payoutInfo.useDefaultValues` | body | `boolean` | no |
