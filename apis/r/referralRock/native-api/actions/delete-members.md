# Delete Members with Referral Rock

Deletes existing members from Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/members/remove`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Delete Members](https://api.referralrock.com/Help/Api/POST-api-members-remove)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no |
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
