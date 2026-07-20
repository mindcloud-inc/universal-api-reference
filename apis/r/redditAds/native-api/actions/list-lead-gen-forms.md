# List Lead Gen Forms with Reddit Lead Ads

Retrieves lead generation forms from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/lead_gen_forms`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Lead Gen Forms](https://ads-api.reddit.com/docs/v3/operations/list-lead-gen-forms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to list lead gen forms for. |
