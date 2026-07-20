# Mark notification as read with MoySklad

Marks a notification as read in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `notification/:id/markasread`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Mark notification as read](https://dev.moysklad.ru/doc/api/remap/1.2/notification/#uwedomleniia-uwedomlenie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MoySklad notification ID. |
