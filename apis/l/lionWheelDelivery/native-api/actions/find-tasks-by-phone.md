# Find Tasks by Phone with LionWheel Delivery

Finds tasks in LionWheel Delivery by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/by_phone/:phone`
- **Base URL:** `https://test.lionwheel.com/api/v1`
- **Official documentation:** [Find Tasks by Phone](https://github.com/lionwheel/api#get-tasks-by-phone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | path | `string` | yes | The recipient phone number to search for. |
