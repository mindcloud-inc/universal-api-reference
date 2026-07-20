# Get a person's groups with xMatters

Retrieves a person's groups from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `people/{personId}/group-memberships`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get a person's groups](https://help.xmatters.com/xmapi/index.html#get-a-person-39-s-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `personId` | path | `string` | no |
