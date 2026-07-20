# Update User Attributes with BotStar

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bots/:botId/users/:userId`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Update User Attributes](https://apis.botstar.com/docs/#/Users/patch_bots__botId__users__userId_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `birthday` | body | `string` | no |
| `botId` | path | `string` | yes |
| `email` | body | `string` | no |
| `first_name` | body | `string` | no |
| `gender` | body | `string` | no |
| `last_name` | body | `string` | no |
| `userId` | path | `string` | yes |
