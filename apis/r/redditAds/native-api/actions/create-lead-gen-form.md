# Create Lead Gen Form with Reddit Lead Ads

Creates a lead generation form in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/lead_gen_forms`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Create Lead Gen Form](https://ads-api.reddit.com/docs/v3/operations/create-lead-gen-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to create the lead gen form under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
