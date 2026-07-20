# Get Order Validation Status with DigiCert

Retrieves validation status for a DigiCert order.

## Endpoint

- **Method:** `GET`
- **Path:** `/order/certificate/:order_id/validation`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [Get Order Validation Status](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | The DigiCert order identifier. |
