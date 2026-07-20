# List RCS Campaigns with smsmode

## Endpoint

- **Method:** `GET`
- **Path:** `rcs/v1/channels/:channelId/campaigns`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [List RCS Campaigns](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/campaigns-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
