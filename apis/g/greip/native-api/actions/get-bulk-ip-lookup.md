# Get Bulk IP Lookup with Greip - Fraud Prevention

Retrieves lookup data for multiple IP addresses from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/ip/bulk`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get Bulk IP Lookup](https://docs.greip.io/api-reference/endpoint/data-lookup/bulk-ip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ips` | query | `string` | yes | Comma-separated IPv4 or IPv6 addresses. Greip documents up to 10 IPs per request. |
| `params` | query | `string` | no | Comma-separated response modules to include, such as security, currency, timezone, location, or device. |
