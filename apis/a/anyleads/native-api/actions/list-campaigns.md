# List Campaigns with Anyleads

Retrieves a list of campaigns from Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/fetch-all-campaigns`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [List Campaigns](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | body | `string` | yes | Campaign state filter. Use all, running, or paused. Accepted values: `0`, `1`, `2`. |
