# Get promo pricing for a plan (public - all users see promo prices) with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/promo/pricing`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get promo pricing for a plan (public - all users see promo prices)](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | query | `string` | yes | The plan ID to get pricing for |
| `currency` | query | `string` | no | Currency for pricing |
