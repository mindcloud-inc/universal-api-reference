# Update Secrets with Doppler Farhan Latif

Updates or creates secrets in a Doppler config.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/configs/config/secrets`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [Update Secrets](https://docs.doppler.com/reference/secrets-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Unique identifier for the project object. |
| `config` | body | `string` | yes | Name of the config object. |
| `secrets` | body | `object` | yes | Object of secrets to save to the config. Either secrets or change_requests is required. |
