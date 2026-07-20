# Archive firmware with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmwares/{id}/archive`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Archive firmware](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `is_archived` | body | `boolean` | yes | Show is this item archived |
