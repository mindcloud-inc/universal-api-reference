# Split Name Batch with Namsor

Retrieves first and last name parts for full names in Namsor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api2/json/parseNameBatch`
- **Base URL:** `https://v2.namsor.com/NamSorAPIv2`
- **Official documentation:** [Split Name Batch](https://namsor.app/api-documentation/split-full-name/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personalNames` | body | `list<object>` | yes | Array of personal name objects. |
