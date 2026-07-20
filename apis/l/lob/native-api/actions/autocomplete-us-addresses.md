# Autocomplete US Addresses with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/us_autocompletions`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Autocomplete US Addresses](https://docs.lob.com/#tag/US-Autocompletions/operation/autocompletion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_prefix` | body | `string` | yes | Partial primary line to autocomplete. |
| `city` | body | `string` | no | Optional city filter. |
| `state` | body | `string` | no | Optional state filter. |
| `zip_code` | body | `string` | no | Optional ZIP code filter. |
| `geo_ip_sort` | body | `boolean` | no | Sort suggestions by client IP proximity when true. |
