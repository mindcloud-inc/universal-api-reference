# Connect Task with iLoveSign

## Endpoint

- **Method:** `POST`
- **Path:** `https://:server/v1/task/next`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Connect Task](https://www.iloveapi.com/docs/api-reference#task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Task-assigned host returned by the start call. |
| `task` | body | `string` | yes | Parent task identifier to connect from. |
| `tool` | body | `string` | yes | Tool to use for the next connected task. |
