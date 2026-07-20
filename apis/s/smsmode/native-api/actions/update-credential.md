# Update Credential with smsmode

## Endpoint

- **Method:** `PATCH`
- **Path:** `commons/v1/channels/:channelId/credentials/:credentialId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Update Credential](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/credential-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `credentialId` | path | `string` | yes | Credential ID path parameter from the smsmode API route. |
| `name` | body | `string` | no | Name request body field documented by the smsmode API. |
| `type` | body | `string` | yes | Type request body field documented by the smsmode API. |
| `roles[]` | body | `array` | no | Roles request body field documented by the smsmode API. |
| `authorizedIps[]` | body | `array` | no | Authorized IPs request body field documented by the smsmode API. |
| `blocked` | body | `boolean` | no | Blocked request body field documented by the smsmode API. |
