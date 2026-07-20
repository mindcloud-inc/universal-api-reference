# Lookup US ZIP Code with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/us_zip_lookups`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Lookup US ZIP Code](https://docs.lob.com/#tag/Zip-Lookups/operation/zip_lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip_code` | body | `string` | yes | 5-digit US ZIP code to look up. |
