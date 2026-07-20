# List Nearby Places by Postal Code with Zippopotamus

Retrieves nearby places in Zippopotamus by postal code.

## Endpoint

- **Method:** `GET`
- **Path:** `/nearby/{{country}}/{{postalcode}}`
- **Base URL:** `https://api.zippopotam.us`
- **Official documentation:** [List Nearby Places by Postal Code](https://docs.zippopotam.us/docs/v1/#places-near-postal-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US. |
| `postalcode` | path | `string` | yes | Postal code used as the center point for nearby places, such as 90210. |
