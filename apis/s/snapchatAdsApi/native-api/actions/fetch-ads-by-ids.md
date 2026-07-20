# Fetch Ads by IDs with Snapchat Ads

Retrieves ads from Snapchat Ads by ad IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/get_ads_by_ids`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Fetch Ads by IDs](https://developers.snap.com/api/marketing-api/Ads-API/ads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the ads. |
| `ad_ids` | body | `list<string>` | yes | An array of Snapchat Ad IDs to fetch. |
