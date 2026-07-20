# Set Bot Field with ManyChat

Updates an existing bot field in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/page/setBotField`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Set Bot Field](https://api.manychat.com/swagger#/Page/4032722e43e4b967e07d1b1279942254)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `field_id` | body | `number` | yes |
| `field_value` | body | `string` | yes |
