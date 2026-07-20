# Get open house (OData) with Bridge Interactive Platform

Retrieves an open house from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/OpenHouse(':OpenHouseKey')`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get open house (OData)](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `OpenHouseKey` | path | `string` | yes | OData open house identifier from Bridge. |
