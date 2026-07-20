# Send Direct SMS with Instasent

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project/channel/sms/sms/direct/:senderId/:audienceId`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Send Direct SMS](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `senderId` | path | `string` | yes | SMS sender identifier. |
| `audienceId` | path | `string` | yes | Audience identifier. |
| `text` | body | `string` | yes | SMS message text. |
| `allowUnicode` | body | `boolean` | no | Whether to allow Unicode characters in the SMS message. |
