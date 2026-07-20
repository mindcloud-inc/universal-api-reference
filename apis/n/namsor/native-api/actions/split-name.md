# Split Name with Namsor

Retrieves first and last name parts from a full name in Namsor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/parseName/:nameFull`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Split Name](https://namsor.app/api-documentation/split-full-name/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nameFull` | path | `string` | yes | Full name input. |
