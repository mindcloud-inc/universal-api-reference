# Name Origin with Namsor

Retrieves the likely country of origin for a name in Namsor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/origin/:firstName/:lastName`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name Origin](https://namsor.app/api-documentation/origin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
