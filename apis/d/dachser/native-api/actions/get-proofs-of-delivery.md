# Get Proofs Of Delivery with Dachser

Retrieves proofs of delivery from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/pods`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Proofs Of Delivery](https://api-portal.dachser.com/bi.b2b.portal/api/library/pod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tracking-number` | query | `string` | yes | Shipment tracking number. |
