# Look Up Places by Postal Code with Zippopotamus

Retrieves places in Zippopotamus by postal code.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{country}}/{{postalcode}}`
- **Base URL:** `https://api.zippopotam.us`
- **Official documentation:** [Look Up Places by Postal Code](https://docs.zippopotam.us/docs/v1/#places-by-postal-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US. |
| `postalcode` | path | `string` | yes | Postal code to query for place data, such as 90210. |
