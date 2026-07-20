# Get IP Lookup with Greip - Fraud Prevention

Retrieves lookup data for an IP address from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/ip`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get IP Lookup](https://docs.greip.io/api-reference/endpoint/data-lookup/ip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | The IPv4 or IPv6 address to inspect. |
| `params` | query | `string` | no | Comma-separated response modules to include, such as security, currency, timezone, location, or device. |
| `lang` | query | `string` | no | Response language. Greip documents EN, AR, DE, FR, ES, JA, ZH, and RU. |
