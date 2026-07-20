# Get Secret with Doppler Farhan Latif

Retrieves a secret from a Doppler config.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs/config/secret`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [Get Secret](https://docs.doppler.com/reference/secrets-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
| `name` | query | `string` | yes | Name of the secret. |
