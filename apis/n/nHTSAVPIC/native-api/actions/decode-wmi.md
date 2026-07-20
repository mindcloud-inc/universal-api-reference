# Decode WMI with NHTSA vPIC

Decodes a WMI with NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/DecodeWMI/:wmi`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [Decode WMI](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wmi` | path | `string` | yes | A 3-character WMI code or 6-character WMI segment to decode. |
