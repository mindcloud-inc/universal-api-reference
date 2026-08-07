# List vehicles with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/vehicles`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List vehicles](https://developer-docs.gomotive.com/reference/list-all-the-company-vehicles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updated_after` | query | `date` | no | Return vehicles updated after the given UTC timestamp. |
