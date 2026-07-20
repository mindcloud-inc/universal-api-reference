# Get a person's devices with xMatters

Retrieves a person's devices from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `people/{personId}/devices`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get a person's devices](https://help.xmatters.com/xmapi/index.html#get-a-person-39-s-devices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `embed` | query | `string` | no |
| `personId` | path | `string` | no |
