# List Membergroups with Webling

## Endpoint

- **Method:** `GET`
- **Path:** `/membergroup`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [List Membergroups](https://demo.webling.ch/api/1#membergroup-membergroup-list-get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Filter the membergroup list using Webling query language. |
| `order` | query | `string` | no | Sort the membergroup list by property and direction. |
| `format` | query | `string` | no | Use full to return full membergroup objects instead of IDs. |
