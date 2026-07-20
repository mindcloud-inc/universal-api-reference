# Get open house with Bridge Interactive Platform

Retrieves an open house from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/openhouses/:openhouseId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get open house](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `openhouseId` | path | `string` | yes | Bridge open house identifier from the REST open houses feed. |
