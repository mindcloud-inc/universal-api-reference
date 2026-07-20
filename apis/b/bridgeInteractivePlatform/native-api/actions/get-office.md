# Get office with Bridge Interactive Platform

Retrieves an office from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/offices/:officeId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get office](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `officeId` | path | `string` | yes | Bridge office identifier from the REST offices feed. |
