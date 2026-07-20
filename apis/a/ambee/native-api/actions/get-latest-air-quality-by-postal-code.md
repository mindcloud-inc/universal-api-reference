# Get Latest Air Quality By Postal Code with Ambee

Retrieves latest air quality data in Ambee by postal code.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest/by-postal-code`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Get Latest Air Quality By Postal Code](https://docs.ambeedata.com/apis/air-quality#latest-postalcode)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postalCode` | query | `string` | yes |
| `countryCode` | query | `string` | yes |
