# Get IP Geolocation with Greip - Fraud Prevention

Retrieves IP geolocation data from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/geoip`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get IP Geolocation](https://docs.greip.io/api-reference/endpoint/data-lookup/geoip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params` | query | `string` | no | Comma-separated response modules to include, such as security, currency, timezone, location, or device. |
| `lang` | query | `string` | no | Response language. Greip documents EN, AR, DE, FR, ES, JA, ZH, and RU. |
