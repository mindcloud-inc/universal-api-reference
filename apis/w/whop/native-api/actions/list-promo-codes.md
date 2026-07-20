# List Promo Codes with Whop

Retrieves promo codes from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/promo_codes`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Promo Codes](https://docs.whop.com/api-reference/promo-codes/list-promo-codes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list promo codes for. |
