# Archive/Unarchive layout with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/dashboards/{id}/archive`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Archive/Unarchive layout](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `is_archived` | body | `boolean` | yes | Show is this item archived |
