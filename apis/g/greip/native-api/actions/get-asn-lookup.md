# Get ASN Lookup with Greip - Fraud Prevention

Retrieves ASN lookup data from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/asn`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get ASN Lookup](https://docs.greip.io/api-reference/endpoint/data-lookup/asn)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asn` | query | `string` | yes | The autonomous system number to look up, such as AS6167 or 6167. |
