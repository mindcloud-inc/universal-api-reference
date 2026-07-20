# List SMS Messages with smsmode

## Endpoint

- **Method:** `GET`
- **Path:** `sms/v1/channels/:channelId/campaigns/:campaignId/messages`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [List SMS Messages](https://dev.smsmode.com/sms/v1/#tag/Message/operation/messages-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | path | `string` | yes | Campaign ID path parameter from the smsmode API route. |
