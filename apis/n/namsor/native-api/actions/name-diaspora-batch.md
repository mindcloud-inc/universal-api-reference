# Name Diaspora Batch with Namsor

Retrieves likely diasporas for names in Namsor by country.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/diasporaBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name Diaspora Batch](https://namsor.app/api-documentation/ethnicity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
