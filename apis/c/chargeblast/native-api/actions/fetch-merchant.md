# Fetch Merchant with Chargeblast

Retrieves a merchant from Chargeblast.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/merchant`
- **Base URL:** `https://api.chargeblast.com`
- **Official documentation:** [Fetch Merchant](https://docs.chargeblast.com/api-reference/enrollment/fetch-merchant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `merchant_id` | query | `string` | no | The merchant ID to fetch. Chargeblast documents this query parameter as optional. |
