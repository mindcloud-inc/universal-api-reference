# Delete Secret with Doppler Farhan Latif

Deletes an existing secret from a Doppler config.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/configs/config/secret`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [Delete Secret](https://docs.doppler.com/reference/secrets-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
| `name` | query | `string` | yes | Name of the secret. |
