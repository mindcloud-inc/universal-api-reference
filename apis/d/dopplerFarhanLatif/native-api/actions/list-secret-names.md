# List Secret Names with Doppler Farhan Latif

Retrieves secret names from a Doppler config.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs/config/secrets/names`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [List Secret Names](https://docs.doppler.com/reference/secrets-names)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `config` | query | `string` | yes | Name of the config object. |
| `include_dynamic_secrets` | query | `boolean` | no | Whether to issue leases and include dynamic secret values. |
| `include_managed_secrets` | query | `boolean` | no | Whether to include Doppler auto-generated managed secrets. |
