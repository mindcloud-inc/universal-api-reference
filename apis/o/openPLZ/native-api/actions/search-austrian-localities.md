# Search Austrian Localities with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/at/Localities`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [Search Austrian Localities](https://www.openplzapi.org/en/austria/#requesting-postal-codes-and-localities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postalCode` | query | `string` | no | Postal code or POSIX regular expression pattern. |
| `name` | query | `string` | no | Locality name or POSIX regular expression pattern. |
