# Match Businesses with Explorium

Matches businesses in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/match`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Match Businesses](https://developers.explorium.ai/reference/businesses/match_businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businesses_to_match[]` | body | `array<object>` | yes | Businesses to match. |
