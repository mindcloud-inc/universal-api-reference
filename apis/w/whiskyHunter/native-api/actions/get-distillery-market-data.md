# Get Distillery Market Data with Whisky Hunter

Retrieves market data for one Whisky Hunter distillery.

## Endpoint

- **Method:** `GET`
- **Path:** `/distillery_data/[:slug]/`
- **Base URL:** `https://whiskyhunter.net/api`
- **Official documentation:** [Get Distillery Market Data](https://whiskyhunter.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Distillery slug from the Whisky Hunter distilleries list, for example ardbeg. |
