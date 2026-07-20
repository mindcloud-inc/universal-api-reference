# List Postal Codes by Place with Zippopotamus

Retrieves postal codes in Zippopotamus by place name.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{country}}/{{state}}/{{place}}`
- **Base URL:** `https://api.zippopotam.us`
- **Official documentation:** [List Postal Codes by Place](https://docs.zippopotam.us/docs/v1/#postal-codes-by-place)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | path | `string` | yes | ISO 3166-1 alpha-2 country code, such as US. |
| `state` | path | `string` | yes | Two-letter state or province abbreviation, such as MA. |
| `place` | path | `string` | yes | Place name, such as Belmont. |
