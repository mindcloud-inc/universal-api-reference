# Get event audit information with xMatters

Retrieves event audit information from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `audits`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get event audit information](https://help.xmatters.com/xmapi/index.html#get-event-audit-information)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `auditType` | query | `string` | no |
| `eventId` | query | `string` | no |
