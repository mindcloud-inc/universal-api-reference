# Delete Referrals with Referral Rock

Deletes existing referrals from Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/referral/remove`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Delete Referrals](https://api.referralrock.com/Help/Api/POST-api-referral-remove)

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
| `items[].query` | body | `object` | yes |
| `items[].query.primaryInfo` | body | `object` | no |
| `items[].query.secondaryInfo` | body | `object` | no |
| `items[].query.tertiaryInfo` | body | `object` | no |
| `items[].query.fuzzyInfo` | body | `object` | no |
