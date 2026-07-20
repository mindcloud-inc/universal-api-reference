# Set User Variable with BotHunter

Updates a BotHunter user variable value.

## Endpoint

- **Method:** `POST`
- **Path:** `/vars/set`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Set User Variable](https://smm.targethunter.help/dev/api/methods/vars/set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `var_id` | body | `string` | yes | ID of the BotHunter user variable to set. |
| `uid` | body | `string` | yes | User ID in the social network or messenger channel. |
| `value` | body | `string` | yes | New value for the user variable. |
