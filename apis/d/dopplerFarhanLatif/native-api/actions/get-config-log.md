# Get Config Log with Doppler Farhan Latif

Retrieves a config log from Doppler.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs/config/logs/log`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [Get Config Log](https://docs.doppler.com/reference/config_logs-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
| `log` | query | `string` | yes | Unique identifier for the log object. |
