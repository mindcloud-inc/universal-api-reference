# Update Referrals with Referral Rock

Updates existing referrals in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/referral/update`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Update Referrals](https://api.referralrock.com/Help/Api/POST-api-referral-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no |
| `items[].query.fuzzyInfo.Identifier` | body | `string` | no |
| `items[].query.primaryInfo.referralId` | body | `string` | no |
| `items[].query.secondaryInfo.email` | body | `string` | no |
| `items[].query.secondaryInfo.externalIdentifier` | body | `string` | no |
| `items[].query.secondaryInfo.phoneNumber` | body | `string` | no |
| `items[].query.tertiaryInfo.ProgramId` | body | `string` | no |
| `items[].query.tertiaryInfo.ProgramName` | body | `string` | no |
| `items[].query.tertiaryInfo.ProgramTitle` | body | `string` | no |
| `items[].referral.companyName` | body | `string` | no |
| `items[].referral.customOption1Name` | body | `string` | no |
| `items[].referral.customOption2Name` | body | `string` | no |
| `items[].referral.customText1Name` | body | `string` | no |
| `items[].referral.customText2Name` | body | `string` | no |
| `items[].referral.customText3Name` | body | `string` | no |
| `items[].referral.email` | body | `string` | no |
| `items[].referral.externalIdentifier` | body | `string` | no |
| `items[].referral.firstName` | body | `string` | no |
| `items[].referral.lastName` | body | `string` | no |
| `items[].referral.note` | body | `string` | no |
| `items[].referral.phoneNumber` | body | `string` | no |
| `items[].referral.preferredContact` | body | `string` | no |
| `items[].referral.publicNote` | body | `string` | no |
| `items[].query` | body | `object` | yes |
| `items[].query.primaryInfo` | body | `object` | no |
| `items[].query.secondaryInfo` | body | `object` | no |
| `items[].query.tertiaryInfo` | body | `object` | no |
| `items[].query.fuzzyInfo` | body | `object` | no |
| `items[].referral` | body | `object` | yes |
| `items[].referral.amount` | body | `number` | no |
