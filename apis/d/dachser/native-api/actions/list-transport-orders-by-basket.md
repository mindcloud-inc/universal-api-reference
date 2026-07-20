# List Transport Orders By Basket with Dachser

Retrieves transport orders from a specific Dachser basket.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/transportorders/{basket}`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [List Transport Orders By Basket](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basket` | path | `string` | yes | Transport order basket. |
| `date-from` | query | `date` | no | Filter transport orders from this date. |
| `date-to` | query | `date` | no | Filter transport orders through this date. |
