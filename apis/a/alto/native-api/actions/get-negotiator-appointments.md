# Get Negotiator Appointments with Alto

Retrieves negotiator appointments from Alto within a selected time range.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments/negotiators`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Negotiator Appointments](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start-date` | query | `date` | yes | Start of the appointment date range. |
| `end-date` | query | `date` | yes | End of the appointment date range. |
| `negotiator-id` | query | `string` | yes | Negotiator identifier whose appointments should be returned. |
