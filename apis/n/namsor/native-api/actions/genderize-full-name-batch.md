# Genderize Full Name Batch with Namsor

Retrieves likely genders for full names in Namsor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/genderFullBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Genderize Full Name Batch](https://namsor.app/api-documentation/gender-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
