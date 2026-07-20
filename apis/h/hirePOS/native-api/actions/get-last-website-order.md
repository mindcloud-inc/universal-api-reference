# Get Last Website Order with HirePOS

Retrieves a customer's last website order from HirePOS by email.

## Endpoint

- **Method:** `GET`
- **Path:** `/LastWebsiteOrder`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Get Last Website Order](https://docs.hirepos.com/en/articles/2314881)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | query | `string` | yes | Email address used to look up the customer's most recent website order. |
