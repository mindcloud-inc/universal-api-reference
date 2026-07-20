# Get text links with Rakuten Advertising

Retrieves text links from Rakuten Advertising.

## Endpoint

- **Method:** `GET`
- **Path:** `/linklocator/1.0/getTextLinks/{advertiserId}/{categoryId}/{linkStartDate}/{linkEndDate}/{campaignId}/{page}`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [Get text links](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/link_locator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advertiserId` | path | `string` | yes | Rakuten advertiser ID. |
| `campaignId` | path | `string` | yes | Deprecated Rakuten campaign ID path slot; use 0 when no value is required. |
| `categoryId` | path | `string` | yes | Creative category ID. |
| `linkEndDate` | path | `string` | yes | End date for link availability in the format expected by Rakuten Link Locator. |
| `linkStartDate` | path | `string` | yes | Start date for link availability in the format expected by Rakuten Link Locator. |
| `page` | path | `number` | yes | Page number. |
