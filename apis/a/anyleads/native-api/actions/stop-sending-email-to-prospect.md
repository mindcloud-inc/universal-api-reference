# Stop Sending Email To Prospect with Anyleads

Updates a prospect to stop receiving emails in Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/stop-sending-email-to-prospect`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Stop Sending Email To Prospect](https://docs.anyleads.com/product/en/sequence-cadence-newsletter-campaigns-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Prospect email to stop from receiving outbound campaigns. |
