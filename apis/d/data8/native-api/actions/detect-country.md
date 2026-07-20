# Detect Country with Data8

Detects a country from contact data in Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/CountryDetection/DetectCountry.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Detect Country](https://docs.data-8.co.uk/web-services/countrydetection/detectcountry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | Structured address and contact data used to detect the country. |
| `options` | body | `object` | no | Optional settings that control country detection behavior. |
