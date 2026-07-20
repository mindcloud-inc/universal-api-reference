# Get Config with Doppler Farhan Latif

Retrieves config details from Doppler.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs/config`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [Get Config](https://docs.doppler.com/reference/configs-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
