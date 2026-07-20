# Remove User From Bot with BotHunter

Deletes a BotHunter bot enrollment for a user in a specified channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/removeUser`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Remove User From Bot](https://smm.targethunter.help/dev/api/methods/bots/removeuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | body | `string` | yes | ID of the BotHunter bot to remove the user from. |
| `uid` | body | `string` | yes | User ID in the social network or messenger channel. |
| `channel` | body | `list<string>` | yes | Channel identifier. Documented values: VK, TG, MAX, OK. Accepted values: `MAX`, `OK`, `TG`, `VK`. |
