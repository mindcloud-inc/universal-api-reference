# Add Email Unsubscribe with Anyleads

Creates an email unsubscribe entry in Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/add-email-unsubscribe`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Add Email Unsubscribe](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to add to the unsubscribe list. |
