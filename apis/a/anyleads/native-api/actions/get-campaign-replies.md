# Get Campaign Replies with Anyleads

Retrieves replies for a campaign from Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/fetch-replies-from-single-campaign`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Get Campaign Replies](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | Campaign identifier returned by List Campaigns. |
