# Genderize Name with Namsor

Retrieves the likely gender for a name in Namsor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/gender/:firstName/:lastName`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Genderize Name](https://namsor.app/api-documentation/gender-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
