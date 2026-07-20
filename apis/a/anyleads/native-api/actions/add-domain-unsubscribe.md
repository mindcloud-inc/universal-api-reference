# Add Domain Unsubscribe with Anyleads

Creates a domain unsubscribe entry in Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/add-domain-unsubscribe`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Add Domain Unsubscribe](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain to add to the unsubscribe list. |
