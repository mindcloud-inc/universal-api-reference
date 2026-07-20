# Get a list of available domains with Routee

Retrieves a list of available domains from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/shorten/domains`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get a list of available domains](https://docs.routee.net/reference/get-a-list-of-available-domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | body | `array<object>` | no | Array of the domain object |
| `name` | body | `string` | no | The domain name |
| `available` | body | `boolean` | no | Whether the domain is available for use or not. |
