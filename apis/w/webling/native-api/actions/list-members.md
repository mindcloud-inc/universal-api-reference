# List Members with Webling

## Endpoint

- **Method:** `GET`
- **Path:** `/member`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [List Members](https://demo.webling.ch/api/1#member-member-list-get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Filter the member list using Webling query language. |
| `order` | query | `string` | no | Sort the member list by property and direction. |
| `format` | query | `string` | no | Use full to return full member objects instead of IDs. |
