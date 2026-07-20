# List RCS Messages with smsmode

## Endpoint

- **Method:** `GET`
- **Path:** `rcs/v1/channels/:channelId/campaigns/:campaignId/messages`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [List RCS Messages](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/messages-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
