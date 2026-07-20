# Name Origin Batch with Namsor

Retrieves likely countries of origin for names in Namsor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/originBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Name Origin Batch](https://namsor.app/api-documentation/origin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
