# Get Contact IDs with Avionte

Retrieves contact IDs from Avionte.

## Endpoint

- **Method:** `GET`
- **Path:** `front-office/v1/contacts/ids/:page/:pageSize`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Get Contact IDs](https://developer.avionte.com/reference/contactids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | path | `number` | yes | The page number to request. |
| `pageSize` | path | `number` | yes | The number of results per page. |
