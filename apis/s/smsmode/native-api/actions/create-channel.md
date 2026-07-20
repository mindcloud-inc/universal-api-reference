# Create Channel with smsmode

## Endpoint

- **Method:** `POST`
- **Path:** `commons/v1/organisations/:organisationId/channels`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Create Channel](https://dev.smsmode.com/commons/v1/#tag/Channel/operation/channel-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationId` | path | `string` | yes | Organisation ID path parameter from the smsmode API route. |
| `name` | body | `string` | yes | Name request body field documented by the smsmode API. |
| `type` | body | `string` | yes | Type request body field documented by the smsmode API. |
| `flow` | body | `string` | yes | Flow request body field documented by the smsmode API. |
| `dailyConsumptionLimit` | body | `number` | no | Daily Consumption Limit request body field documented by the smsmode API. |
| `defaultCallbackUrlStatus` | body | `string` | no | Default Status Callback URL request body field documented by the smsmode API. |
| `defaultCallbackUrlMo` | body | `string` | no | Default MO Callback URL request body field documented by the smsmode API. |
