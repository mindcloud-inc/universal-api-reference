# List Documentgroups with Webling

## Endpoint

- **Method:** `GET`
- **Path:** `/documentgroup`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [List Documentgroups](https://demo.webling.ch/api/1#documentgroup-documentgroup-list-get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Filter the document group list using Webling query language. |
| `order` | query | `string` | no | Sort the document group list by property and direction. |
| `format` | query | `string` | no | Optional Webling response format. |
