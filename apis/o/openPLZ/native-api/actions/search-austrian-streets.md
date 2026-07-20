# Search Austrian Streets with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/at/Streets`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [Search Austrian Streets](https://www.openplzapi.org/en/austria/#requesting-streets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Street name or POSIX regular expression pattern. |
| `postalCode` | query | `string` | no | Postal code or POSIX regular expression pattern. |
| `locality` | query | `string` | no | Locality name or POSIX regular expression pattern. |
