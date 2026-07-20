# Clear Community Variable with BotHunter

Deletes the value of a BotHunter community variable.

## Endpoint

- **Method:** `POST`
- **Path:** `/globalvars/clear`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Clear Community Variable](https://smm.targethunter.help/dev/api/methods/globalvars/clear)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `var_id` | body | `string` | yes | ID of the BotHunter community variable to clear. |
