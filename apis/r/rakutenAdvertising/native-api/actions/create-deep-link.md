# Create deep link with Rakuten Advertising

Creates a deep link in Rakuten Advertising.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links/deep_links`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [Create deep link](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/deep_link)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advertiser_id` | body | `number` | yes | Rakuten advertiser ID for the deep link. |
| `url` | body | `string` | yes | Destination URL to turn into a Rakuten deep link. |
