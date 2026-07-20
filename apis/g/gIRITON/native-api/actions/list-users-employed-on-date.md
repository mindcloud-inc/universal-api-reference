# List Users Employed On Date with GIRITON

Retrieves users employed on a selected GIRITON date.

## Endpoint

- **Method:** `GET`
- **Path:** `/hr/usersEmployedOn`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Users Employed On Date](https://rest.giriton.com/apidoc/#/Human%20Resources/getUsersEmployedOn)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `day` | query | `string` | no | Day on which users should be employed. If omitted, GIRITON uses today. |
