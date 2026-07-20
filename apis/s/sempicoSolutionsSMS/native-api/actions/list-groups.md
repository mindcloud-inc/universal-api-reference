# List Groups with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/group`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [List Groups](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Number of groups to return. |
| `offset` | body | `number` | no | Page offset for group listing. |
| `id_group` | body | `number` | no | Optional group ID to return one specific group. |
