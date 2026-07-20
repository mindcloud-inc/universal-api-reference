# Retrieve Contact with Fleetio

Retrieves a specific contact from Fleetio.

## Endpoint

- **Method:** `GET`
- **Path:** `contacts/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Retrieve Contact](https://developer.fleetio.com/docs/api/contacts-show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the relevant record |
| `expand[]` | query | `array<string>` | no | Additional attributes that should be returned in the response. Available: `group` |
