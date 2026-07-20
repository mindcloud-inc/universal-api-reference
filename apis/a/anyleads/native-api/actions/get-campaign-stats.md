# Get Campaign Stats with Anyleads

Retrieves statistics for a campaign from Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/fetch-stats-from-single-campaign`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Get Campaign Stats](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | Campaign identifier returned by List Campaigns. |
