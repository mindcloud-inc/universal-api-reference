# List Configs with Doppler Farhan Latif

Retrieves configs from a Doppler project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/configs`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [List Configs](https://docs.doppler.com/reference/configs-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | The project's name. |
| `environment` | query | `string` | no | Optional environment slug from which to list configs. |
