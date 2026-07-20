# Fetch Ad Squads by IDs with Snapchat Ads

Retrieves ad squads from Snapchat Ads by ad squad IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/get_adsquads_by_ids`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Fetch Ad Squads by IDs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the ad squads. |
| `adsquad_ids` | body | `list<string>` | yes | An array of Snapchat Ad Squad IDs to fetch. |
