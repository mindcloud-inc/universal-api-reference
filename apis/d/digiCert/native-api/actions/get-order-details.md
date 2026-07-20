# Get Order Details with DigiCert

Retrieves details for a certificate order in DigiCert.

## Endpoint

- **Method:** `GET`
- **Path:** `/order/certificate/:order_id`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [Get Order Details](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | The DigiCert order identifier. |
