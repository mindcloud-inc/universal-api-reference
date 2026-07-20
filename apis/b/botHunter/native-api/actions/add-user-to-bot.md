# Add User To Bot with BotHunter

Creates a BotHunter bot enrollment for a user in a specified channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/addUser`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Add User To Bot](https://smm.targethunter.help/dev/api/methods/bots/adduser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | body | `string` | yes | ID of the BotHunter bot to add the user to. |
| `uid` | body | `string` | yes | User ID in the social network or messenger channel. |
| `channel` | body | `list<string>` | yes | Channel identifier. Documented values: VK, TG, MAX, OK. Accepted values: `MAX`, `OK`, `TG`, `VK`. |
| `step_id` | body | `string` | no | Optional BotHunter step ID to add the user to. |
| `force` | body | `list<string>` | no | Use 1 to add the user even if they are already in the bot; use 0 otherwise. Accepted values: `0`, `1`. |
| `payload` | body | `object` | no | Optional additional parameters to pass into the bot. BotHunter accepts a string or structured payload. |
