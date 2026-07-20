# Get events with xMatters

Retrieves events from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `events`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get events](https://help.xmatters.com/xmapi/index.html#get-events)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `embed` | query | `string` | no |
| `priority` | query | `string` | no |
| `propertyName` | query | `string` | no |
| `propertyValue` | query | `string` | no |
