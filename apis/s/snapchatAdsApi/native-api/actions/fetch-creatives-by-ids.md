# Fetch Creatives by IDs with Snapchat Ads

Retrieves creatives from Snapchat Ads by creative IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/get_creatives_by_ids`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Fetch Creatives by IDs](https://developers.snap.com/api/marketing-api/Ads-API/creatives)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the creatives. |
| `creative_ids` | body | `list<string>` | yes | An array of Snapchat Creative IDs to fetch. |
