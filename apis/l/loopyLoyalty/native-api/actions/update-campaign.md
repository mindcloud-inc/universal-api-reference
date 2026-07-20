# Update Campaign with Loopy Loyalty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaign/:id`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Update Campaign](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_updateCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign ID to update. |
| `campaignName` | body | `string` | yes | Updated campaign name. |
| `description` | body | `string` | yes | Updated campaign description. |
| `organisationName` | body | `string` | yes | Organisation name shown on the campaign. |
| `businessAddressLine1` | body | `string` | yes | Primary street address for the business. |
| `businessCity` | body | `string` | yes | City for the business address. |
| `businessCountry` | body | `string` | yes | Two-letter country code for the business. |
| `businessEmail` | body | `string` | yes | Contact email for the business. |
| `businessStateProvinceRegion` | body | `string` | yes | State, province, or region for the business. |
| `businessWebsite` | body | `string` | yes | Website URL for the business. |
| `collectValue` | body | `string` | yes | Updated stamp collection rule. |
| `rewardName` | body | `string` | yes | Updated reward name. |
| `rewardText` | body | `string` | yes | Updated reward description. |
| `stampsRequired` | body | `number` | yes | Number of stamps required to earn the reward. |
| `uniqueEmailFieldName` | body | `string` | no | Field name to enforce as the campaign's unique email identifier. |
| `uniquePhoneFieldName` | body | `string` | no | Field name to enforce as the campaign's unique phone identifier. |
| `status` | body | `number` | no | Campaign status: 1 for draft, 2 for published. |
