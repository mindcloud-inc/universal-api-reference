# Get User Variable with BotHunter

Retrieves a BotHunter user variable value.

## Endpoint

- **Method:** `GET`
- **Path:** `/vars/get`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Get User Variable](https://smm.targethunter.help/dev/api/methods/vars/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `var_id` | query | `string` | yes | ID of the BotHunter user variable to read. |
| `uid` | query | `string` | yes | User ID in the social network or messenger channel. |
