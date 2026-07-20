# Create Bot Field with ManyChat

Creates a new bot field in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/page/createBotField`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Create Bot Field](https://api.manychat.com/swagger#/Page/388714b65c83021aa8b1bb78481fb983)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
| `description` | body | `string` | no |
| `value` | body | `string` | no |
