# Full Name Country with Namsor

Retrieves the likely country of residence for a full name in Namsor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/country/:personalNameFull`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Full Name Country](https://namsor.app/api-documentation/country-of-residence/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNameFull` | path | `string` | yes | Full personal name. |
