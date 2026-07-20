# Update Contact Scoring with Anyleads

Updates an existing contact's scoring in Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/update-a-contact-scoring`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Update Contact Scoring](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email used to identify the record whose score should change. |
| `score` | body | `number` | yes | New score value for the contact. |
