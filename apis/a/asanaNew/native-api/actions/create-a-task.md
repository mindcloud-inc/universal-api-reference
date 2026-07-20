# Create a task with Asana

Creates a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a task](https://developers.asana.com/reference/createtask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
