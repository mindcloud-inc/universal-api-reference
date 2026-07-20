# List offers with Rakuten Advertising

Retrieves offers from Rakuten Advertising.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/offers`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [List offers](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis/offers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offer_status` | query | `string` | yes | Required Rakuten offer status filter, such as active, upcoming, or expired. |
