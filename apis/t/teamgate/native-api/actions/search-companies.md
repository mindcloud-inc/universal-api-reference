# Search Companies with Teamgate

Finds companies in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Search Companies](https://developers.teamgate.com/#5123441a-7bc1-4ab6-a79d-42e536804a91)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name[like]` | query | `string` | no | Substring to match in the company name. |
