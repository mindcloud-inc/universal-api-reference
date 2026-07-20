# Fetch Campaigns by IDs with Snapchat Ads

Retrieves campaigns from Snapchat Ads by campaign IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/get_campaigns_by_ids`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Fetch Campaigns by IDs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the campaigns. |
| `campaign_ids` | body | `list<string>` | yes | An array of Snapchat Campaign IDs to fetch. |
