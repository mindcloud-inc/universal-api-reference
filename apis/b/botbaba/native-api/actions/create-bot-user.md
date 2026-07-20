# Create Bot User with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/InsertBotUser`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Create Bot User](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | body | `number` | yes | Bot identifier. |
| `name` | body | `string` | yes | Bot user name. |
| `mobile` | body | `string` | no | Bot user mobile number. |
| `email` | body | `string` | no | Bot user email. |
| `gender` | body | `string` | no | Bot user gender. |
