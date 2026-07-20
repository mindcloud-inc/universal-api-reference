# Get user delivery data with xMatters

Retrieves user delivery data from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `events/{eventId}/user-deliveries`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get user delivery data](https://help.xmatters.com/xmapi/index.html#get-user-delivery-data)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `at` | query | `string` | no |
| `embed` | query | `string` | no |
| `eventId` | path | `string` | no |
