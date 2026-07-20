# List Groups with Seven

Retrieves groups from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [List Groups](https://docs.seven.io/en/rest-api/endpoints/groups#list-all-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | yes | Limit the number of groups returned. |
| `offset` | query | `number` | yes | The starting point from which the list should be displayed. |
