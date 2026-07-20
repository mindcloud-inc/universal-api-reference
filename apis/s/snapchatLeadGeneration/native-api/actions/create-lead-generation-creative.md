# Create Lead Generation Creative with Snapchat Lead Generation

Creates a lead generation creative in Snapchat Lead Generation.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/creatives`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Lead Generation Creative](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#creating-a-lead-generation-creative-using-a-lead-generation-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that will own the new lead generation creative. |
| `creatives` | body | `list<object>` | yes | An array of creative objects for Snapchat lead generation creatives. |
