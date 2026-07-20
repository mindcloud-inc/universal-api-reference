# List Events with Follow Up Boss - Legacy

Retrieves events from Follow Up Boss - Legacy.

## Endpoint

- **Method:** `GET`
- **Path:** `events`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [List Events](https://docs.followupboss.com/reference/events-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createDate` | query | `string` | no |
| `hasProperty` | query | `boolean` | no |
| `next` | query | `string` | no |
| `personId` | query | `int32` | no |
| `propertyAddress` | query | `string` | no |
| `type` | query | `string` | no |
