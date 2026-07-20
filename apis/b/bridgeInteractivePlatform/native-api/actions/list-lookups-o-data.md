# List lookups (OData) with Bridge Interactive Platform

Retrieves lookup records from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/Lookup`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List lookups (OData)](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
