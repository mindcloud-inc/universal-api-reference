# Set Community Variable with BotHunter

Updates a BotHunter community variable value.

## Endpoint

- **Method:** `POST`
- **Path:** `/globalvars/set`
- **Base URL:** `https://smm.targethunter.ru/api`
- **Official documentation:** [Set Community Variable](https://smm.targethunter.help/dev/api/methods/globalvars/set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `var_id` | body | `string` | yes | ID of the BotHunter community variable to set. |
| `value` | body | `string` | yes | New value for the community variable. |
