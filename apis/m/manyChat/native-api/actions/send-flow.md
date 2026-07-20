# Send Flow with ManyChat

Sends an automation flow in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/sending/sendFlow`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Send Flow](https://api.manychat.com/swagger#/Sending/28f1abbb07b0d4773b846dbeb3880e3c)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `flow_ns` | body | `string` | yes |
