# List Tasks with iLovePDF

Retrieves tasks from iLovePDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [List Tasks](https://www.iloveapi.com/docs/api-reference#task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | Task results page number. iLovePDF returns 50 results per page. |
| `tool` | body | `string` | no | Filter tasks by iLovePDF tool key such as merge or compress. |
| `status` | body | `string` | no | Filter tasks by task status such as TaskSuccess. |
| `custom_int` | body | `number` | no | Filter tasks by the custom integer metadata value stored on the task. |
