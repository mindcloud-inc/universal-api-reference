# Update Channel with smsmode

## Endpoint

- **Method:** `PATCH`
- **Path:** `commons/v1/organisations/:organisationId/channels/:channelId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Update Channel](https://dev.smsmode.com/commons/v1/#tag/Channel/operation/channel-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationId` | path | `string` | yes | Organisation ID path parameter from the smsmode API route. |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `name` | body | `string` | no | Name request body field documented by the smsmode API. |
| `dailyConsumptionLimit` | body | `number` | no | Daily Consumption Limit request body field documented by the smsmode API. |
| `defaultCallbackUrlStatus` | body | `string` | no | Default Status Callback URL request body field documented by the smsmode API. |
| `defaultCallbackUrlMo` | body | `string` | no | Default MO Callback URL request body field documented by the smsmode API. |
