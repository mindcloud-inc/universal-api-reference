# Search Swiss Localities with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/ch/Localities`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [Search Swiss Localities](https://www.openplzapi.org/en/switzerland/#requesting-postal-codes-and-localities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postalCode` | query | `string` | no | Postal code or POSIX regular expression pattern. |
| `name` | query | `string` | no | Locality name or POSIX regular expression pattern. |
