# Create User Attribute with BotStar

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/users/attributes`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Create User Attribute](https://apis.botstar.com/docs/#/Users/post_bots__botId__users_attributes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `string` | yes |
| `field_name` | body | `string` | yes |
| `field_type` | body | `string` | yes |
