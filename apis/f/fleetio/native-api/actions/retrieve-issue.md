# Retrieve Issue with Fleetio

Retrieves a specific issue from Fleetio.

## Endpoint

- **Method:** `GET`
- **Path:** `issues/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Retrieve Issue](https://developer.fleetio.com/docs/api/issues-show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the relevant record |
| `includes` | query | `string` | no | A comma-separated list of additional attributes to include in the response. |
