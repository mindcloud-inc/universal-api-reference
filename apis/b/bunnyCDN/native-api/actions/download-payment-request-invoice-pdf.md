# Download Payment Request Invoice PDF with BunnyCDN

Retrieves a BunnyCDN payment request invoice PDF.

## Endpoint

- **Method:** `GET`
- **Path:** `/billing/payment-request-invoice/:id/pdf`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Download Payment Request Invoice PDF](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny payment request identifier. |
