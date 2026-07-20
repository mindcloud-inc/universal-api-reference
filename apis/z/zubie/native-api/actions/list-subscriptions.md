# List Subscriptions with Zubie

Retrieves subscriptions from Zubie.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [List Subscriptions](https://developer.zubie.com/reference/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor for pagination. |
| `size` | query | `string` | no | Number of results to return. |
