# Get Freight Costs with Dachser

Retrieves freight costs for a consignment from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/freightcosts`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Freight Costs](https://api-portal.dachser.com/bi.b2b.portal/api/library/freightcosts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tracking-number` | query | `string` | yes | Shipment tracking number. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
