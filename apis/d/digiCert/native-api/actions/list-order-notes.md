# List Order Notes with DigiCert

Retrieves notes for a DigiCert certificate order.

## Endpoint

- **Method:** `GET`
- **Path:** `/order/certificate/:order_id/note`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [List Order Notes](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | The DigiCert order identifier. |
