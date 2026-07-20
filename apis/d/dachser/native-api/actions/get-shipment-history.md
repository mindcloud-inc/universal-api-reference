# Get Shipment History with Dachser

Retrieves shipment history details from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/shipmenthistory`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Shipment History](https://api-portal.dachser.com/bi.b2b.portal/api/library/shipmenthistory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tracking-number` | query | `string` | yes | Shipment tracking number. |
| `customer-id` | query | `string` | no | Optional customer ID. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
