# Name US Race Ethnicity Batch with Namsor

Retrieves likely US race and ethnicity for names in Namsor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/usRaceEthnicityBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name US Race Ethnicity Batch](https://namsor.app/api-documentation/us-race-ethnicity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
