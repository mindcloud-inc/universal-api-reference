# Delete Groups with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/group-delete`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Delete Groups](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_group[]` | body | `array<number>` | yes | Group IDs to delete. |
