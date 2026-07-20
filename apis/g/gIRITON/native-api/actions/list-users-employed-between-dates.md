# List Users Employed Between Dates with GIRITON

Retrieves users employed during a selected GIRITON date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/hr/usersEmployedBetween`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Users Employed Between Dates](https://rest.giriton.com/apidoc/#/Human%20Resources/getUsersEmployedBetween)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employedFrom` | query | `string` | no | Start of the employment interval. |
| `employedTo` | query | `string` | no | End of the employment interval. |
