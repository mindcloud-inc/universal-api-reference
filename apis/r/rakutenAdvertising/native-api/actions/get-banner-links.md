# Get banner links with Rakuten Advertising

Retrieves banner links from Rakuten Advertising.

## Endpoint

- **Method:** `GET`
- **Path:** `/linklocator/1.0/getBannerLinks/{advertiserId}/{categoryId}/{linkStartDate}/{linkEndDate}/{bannerSizeCode}/{campaignId}/{page}`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [Get banner links](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advertiserId` | path | `string` | yes | Rakuten advertiser ID. |
| `bannerSizeCode` | path | `string` | yes | Rakuten banner size code. |
| `campaignId` | path | `string` | yes | Deprecated Rakuten campaign ID path slot; use 0 when no value is required. |
| `categoryId` | path | `string` | yes | Creative category ID. |
| `linkEndDate` | path | `string` | yes | End date for link availability in the format expected by Rakuten Link Locator. |
| `linkStartDate` | path | `string` | yes | Start date for link availability in the format expected by Rakuten Link Locator. |
| `page` | path | `number` | yes | Page number. |
