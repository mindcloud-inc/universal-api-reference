# Create Lead Generation Form with Snapchat Lead Generation

Creates a lead generation form in Snapchat Lead Generation.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/lead_generation_forms`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Lead Generation Form](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#creating-a-lead-generation-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that will own the new lead generation form. |
| `lead_generation_forms` | body | `list<object>` | yes | An array of lead generation form objects as documented by Snapchat. |
