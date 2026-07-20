# Get Lead Replies with Anyleads

Retrieves replies for a lead from Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/fetch-replies-from-single-lead`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Get Lead Replies](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Lead email address whose replies should be fetched. |
