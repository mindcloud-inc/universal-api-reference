# Search Swiss Streets with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/ch/Streets`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [Search Swiss Streets](https://www.openplzapi.org/en/switzerland/#requesting-streets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Street name or POSIX regular expression pattern. |
| `postalCode` | query | `string` | no | Postal code or POSIX regular expression pattern. |
| `locality` | query | `string` | no | Locality name or POSIX regular expression pattern. |
