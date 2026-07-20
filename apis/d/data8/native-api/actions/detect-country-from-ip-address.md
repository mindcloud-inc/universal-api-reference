# Detect Country from IP Address with Data8

Detects a country from an IP address in Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/CountryDetection/IPAddressToCountrySimple.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Detect Country from IP Address](https://docs.data-8.co.uk/web-services/countrydetection/ipaddresstocountrysimple)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | body | `string` | yes | The IP address to detect the country from. |
