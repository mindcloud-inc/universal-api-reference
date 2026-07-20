# List Donors with Donorbox

Retrieves donors from Donorbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/donors`
- **Base URL:** `https://donorbox.org/api/v1`
- **Official documentation:** [List Donors](https://github.com/donorbox/donorbox-api#donors)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter donors by Donorbox donor ID. |
| `first_name` | query | `string` | no | Filter donors by first name. |
| `last_name` | query | `string` | no | Filter donors by last name. |
| `email` | query | `string` | no | Filter donors by email. |
