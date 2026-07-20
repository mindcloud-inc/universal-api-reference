# Show Receipt with One-Time Secret

Retrieves a secret receipt from One-Time Secret by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/receipt/:identifier`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Show Receipt](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_showreceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Receipt identifier to retrieve. |
