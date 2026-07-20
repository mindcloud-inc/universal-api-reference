# Get Claim History with Mercado Pago

Retrieves claim status history from Mercado Pago.

## Endpoint

- **Method:** `GET`
- **Path:** `/post-purchase/v1/claims/{claim_id}/status_history`
- **Base URL:** `https://api.mercadopago.com`
- **Official documentation:** [Get Claim History](https://www.mercadopago.com.ar/developers/en/reference/claims/get-claim-history/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `claim_id` | path | `number` | yes |
