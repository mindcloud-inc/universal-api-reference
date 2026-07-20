# List Aircraft Fleets with Airlabs

Retrieves airline fleet data from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/fleets`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Aircraft Fleets](https://airlabs.co/docs/fleets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airline_iata` | query | `string` | no | Filter by airline IATA code. |
| `reg_number` | query | `string` | no | Filter by aircraft registration number. |
