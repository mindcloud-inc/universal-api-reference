# List Tasks with iLoveSign

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [List Tasks](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | One-based task results page. |
| `tool` | body | `string` | no | Optional task tool filter, such as split or compress. |
| `status` | body | `string` | no | Optional task status filter, such as TaskSuccess. |
| `custom_int` | body | `number` | no | Optional custom_int filter value. |
