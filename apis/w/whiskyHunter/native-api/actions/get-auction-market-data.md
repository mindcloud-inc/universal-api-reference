# Get Auction Market Data with Whisky Hunter

Retrieves aggregated market data for one Whisky Hunter auction.

## Endpoint

- **Method:** `GET`
- **Path:** `/auction_data/[:slug]/`
- **Base URL:** `https://whiskyhunter.net/api`
- **Official documentation:** [Get Auction Market Data](https://whiskyhunter.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Auction slug from the Whisky Hunter auctions list, for example catawiki. |
