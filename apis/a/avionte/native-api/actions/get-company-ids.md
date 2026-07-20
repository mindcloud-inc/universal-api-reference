# Get Company IDs with Avionte

Retrieves company IDs from Avionte.

## Endpoint

- **Method:** `GET`
- **Path:** `front-office/v1/companies/ids/:page/:pageSize`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Get Company IDs](https://developer.avionte.com/reference/companyids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | path | `number` | yes | The page number to request. |
| `pageSize` | path | `number` | yes | The number of results per page. |
