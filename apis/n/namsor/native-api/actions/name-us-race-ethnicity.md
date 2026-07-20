# Name US Race Ethnicity with Namsor

Retrieves likely US race and ethnicity for a name in Namsor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/usRaceEthnicity/:firstName/:lastName`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name US Race Ethnicity](https://namsor.app/api-documentation/us-race-ethnicity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
