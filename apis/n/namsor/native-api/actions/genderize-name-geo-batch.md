# Genderize Name Geo Batch with Namsor

Retrieves likely genders for names in Namsor by country.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/genderGeoBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Genderize Name Geo Batch](https://namsor.app/api-documentation/gender-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
