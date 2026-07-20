# Show Secret with One-Time Secret

Retrieves secret metadata from One-Time Secret by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/secret/:identifier`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Show Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_showsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Secret identifier to retrieve. |
