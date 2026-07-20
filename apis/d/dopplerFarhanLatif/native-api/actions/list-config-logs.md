# List Config Logs with Doppler Farhan Latif

Retrieves config logs from Doppler.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs/config/logs`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [List Config Logs](https://docs.doppler.com/reference/config_logs-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
