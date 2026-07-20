# List Duplicates with DigiCert

Retrieves duplicate certificates for a DigiCert order.

## Endpoint

- **Method:** `GET`
- **Path:** `/order/certificate/:order_id/duplicate`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [List Duplicates](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | The DigiCert order identifier. |
