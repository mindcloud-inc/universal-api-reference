# Create Campaign with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Create Campaign](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignName` | body | `string` | yes | Name of the campaign to create. |
| `description` | body | `string` | yes | Description for the campaign. |
| `organisationName` | body | `string` | yes | Organisation name shown on the campaign. |
| `businessAddressLine1` | body | `string` | yes | Primary street address for the business. |
| `businessCity` | body | `string` | yes | City for the business address. |
| `businessCountry` | body | `string` | yes | Two-letter country code for the business. |
| `businessEmail` | body | `string` | yes | Contact email for the business. |
| `businessStateProvinceRegion` | body | `string` | yes | State, province, or region for the business. |
| `businessWebsite` | body | `string` | yes | Website URL for the business. |
| `collectValue` | body | `string` | yes | What the customer must do to collect one stamp. |
| `rewardName` | body | `string` | yes | Name of the reward customers earn. |
| `rewardText` | body | `string` | yes | Description of the reward customers earn. |
| `stampsRequired` | body | `number` | yes | Number of stamps required to earn the reward. |
