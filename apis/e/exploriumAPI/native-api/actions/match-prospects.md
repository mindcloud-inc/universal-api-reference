# Match Prospects with Explorium

Matches prospects in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/match`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Match Prospects](https://developers.explorium.ai/reference/prospects/match_prospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prospects_to_match[]` | body | `array<object>` | yes | Prospects to match. |
