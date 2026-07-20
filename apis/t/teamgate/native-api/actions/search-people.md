# Search People with Teamgate

Finds people in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/people`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Search People](https://developers.teamgate.com/#7708cc10-52d4-4ec3-bcc5-1222f21480bb)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name[like]` | query | `string` | no | Substring to match in the person name. |
