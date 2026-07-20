# Create Credential with smsmode

## Endpoint

- **Method:** `POST`
- **Path:** `commons/v1/channels/:channelId/credentials`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Create Credential](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/credential-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Channel ID path parameter from the smsmode API route. |
| `name` | body | `string` | yes | Name request body field documented by the smsmode API. |
| `type` | body | `string` | yes | Type request body field documented by the smsmode API. |
| `roles[]` | body | `array` | yes | Roles request body field documented by the smsmode API. |
| `authorizedIps[]` | body | `array` | no | Authorized IPs request body field documented by the smsmode API. |
