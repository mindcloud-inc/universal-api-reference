# List Secrets with Doppler Farhan Latif

Retrieves secrets from a Doppler config.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs/config/secrets`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [List Secrets](https://docs.doppler.com/reference/secrets-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
| `include_dynamic_secrets` | query | `boolean` | no | Whether to issue leases and include dynamic secret values. |
| `dynamic_secrets_ttl_sec` | query | `number` | no | Seconds until dynamic leases expire. Must be used with Include Dynamic Secrets. |
| `secrets` | query | `string` | no | Comma-separated list of secrets to include in the response. |
| `include_managed_secrets` | query | `boolean` | no | Whether to include Doppler auto-generated managed secrets. |
