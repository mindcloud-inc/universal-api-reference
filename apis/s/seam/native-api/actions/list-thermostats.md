# List Thermostats with Seam

Retrieves a list of thermostats from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/thermostats/list`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [List Thermostats](https://docs.seam.co/latest/api/thermostats/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connected_account_id` | body | `string` | no | ID of the connected account for which you want to list thermostats. |
| `search` | body | `string` | no | Search string for thermostats. |
| `space_id` | body | `string` | no | ID of the space for which you want to list thermostats. |
