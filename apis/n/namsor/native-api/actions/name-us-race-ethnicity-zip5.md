# Name US Race Ethnicity ZIP5 with Namsor

Retrieves likely US race and ethnicity for a name in Namsor by ZIP5.

## Endpoint

- **Method:** `GET`
- **Path:** `/api2/json/usRaceEthnicityZIP5/:firstName/:lastName/:zip5Code`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name US Race Ethnicity ZIP5](https://namsor.app/api-documentation/us-race-ethnicity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | path | `string` | yes | First name. |
| `lastName` | path | `string` | yes | Last name. |
| `zip5Code` | path | `string` | yes | 5-digit ZIP code. |
