# Create Custom Field with ManyChat

Creates a new custom field in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/page/createCustomField`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Create Custom Field](https://api.manychat.com/swagger#/Page/1d7171252e09f4e25b5123f9484ea3c1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `caption` | body | `string` | yes |
| `type` | body | `string` | yes |
| `description` | body | `string` | no |
