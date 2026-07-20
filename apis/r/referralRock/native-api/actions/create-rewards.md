# Create Rewards with Referral Rock

Creates new rewards in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rewards`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Create Rewards](https://api.referralrock.com/Help/Api/POST-api-rewards)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no |
| `items[].memberQuery.primaryInfo.memberId` | body | `string` | no |
| `items[].memberQuery.primaryInfo.referralCode` | body | `string` | no |
| `items[].memberQuery.secondaryInfo.email` | body | `string` | no |
| `items[].memberQuery.secondaryInfo.externalIdentifier` | body | `string` | no |
| `items[].memberQuery.tertiaryInfo.programId` | body | `string` | no |
| `items[].memberQuery.tertiaryInfo.programName` | body | `string` | no |
| `items[].memberQuery.tertiaryInfo.programTitle` | body | `string` | no |
| `items[].newReward.description` | body | `string` | no |
| `items[].referralQuery.fuzzyInfo.Identifier` | body | `string` | no |
| `items[].referralQuery.primaryInfo.referralId` | body | `string` | no |
| `items[].referralQuery.secondaryInfo.email` | body | `string` | no |
| `items[].referralQuery.secondaryInfo.externalIdentifier` | body | `string` | no |
| `items[].referralQuery.secondaryInfo.phoneNumber` | body | `string` | no |
| `items[].referralQuery.tertiaryInfo.ProgramId` | body | `string` | no |
| `items[].referralQuery.tertiaryInfo.ProgramName` | body | `string` | no |
| `items[].referralQuery.tertiaryInfo.ProgramTitle` | body | `string` | no |
| `items[].memberQuery` | body | `object` | no |
| `items[].memberQuery.primaryInfo` | body | `object` | no |
| `items[].memberQuery.secondaryInfo` | body | `object` | no |
| `items[].memberQuery.tertiaryInfo` | body | `object` | no |
| `items[].referralQuery` | body | `object` | no |
| `items[].referralQuery.primaryInfo` | body | `object` | no |
| `items[].referralQuery.secondaryInfo` | body | `object` | no |
| `items[].referralQuery.tertiaryInfo` | body | `object` | no |
| `items[].referralQuery.fuzzyInfo` | body | `object` | no |
| `items[].newReward` | body | `object` | yes |
| `items[].newReward.amount` | body | `number` | no |
| `items[].newReward.payoutId` | body | `string` | yes |
| `items[].newReward.eligibilityDate` | body | `date` | no |
