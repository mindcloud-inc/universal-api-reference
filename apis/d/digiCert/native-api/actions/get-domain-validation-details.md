# Get Domain Validation Details with DigiCert

Retrieves validation details for a domain in DigiCert.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/:domain_id/validation`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [Get Domain Validation Details](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | path | `string` | yes | The DigiCert domain identifier. |
