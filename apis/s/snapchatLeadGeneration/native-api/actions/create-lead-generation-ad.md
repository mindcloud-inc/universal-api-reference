# Create Lead Generation Ad with Snapchat Lead Generation

Creates a lead generation ad in Snapchat Lead Generation.

## Endpoint

- **Method:** `POST`
- **Path:** `/adsquads/:adSquadId/ads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Lead Generation Ad](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#creating-a-lead-generation-ad-using-a-creative)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adSquadId` | path | `string` | yes | The Snapchat Ad Squad ID that will own the new lead generation ad. |
| `ads` | body | `list<object>` | yes | An array of ad objects for Snapchat lead generation ads. |
