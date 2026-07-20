# List Domain DCV Methods with DigiCert

Retrieves available domain DCV methods from DigiCert.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/:domain_id/dcv/method`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [List Domain DCV Methods](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | path | `string` | yes | The DigiCert domain identifier. |
