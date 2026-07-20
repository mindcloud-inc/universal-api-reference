# Full Name Country Batch with Namsor

Retrieves likely countries of residence for full names in Namsor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/countryBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Full Name Country Batch](https://namsor.app/api-documentation/country-of-residence/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
