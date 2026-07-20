# List Subscriptions By Plan with Sendcrux

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/subscriptions`
- **Base URL:** `https://sendcrux.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | The page number of subscriptions to return. |
| `per_page` | query | `string` | no | The number of subscriptions to return per page. |
| `plan_uid` | query | `string` | yes | Filter subscriptions to a specific plan uid. |
