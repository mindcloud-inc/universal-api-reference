# Clear User Variable with BotHunter

Deletes the value of a BotHunter user variable.

## Endpoint

- **Method:** `POST`
- **Path:** `/vars/clear`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Clear User Variable](https://smm.targethunter.help/dev/api/methods/vars/clear)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `var_id` | body | `string` | yes | ID of the BotHunter user variable to clear. |
| `uid` | body | `string` | yes | User ID in the social network or messenger channel. |
