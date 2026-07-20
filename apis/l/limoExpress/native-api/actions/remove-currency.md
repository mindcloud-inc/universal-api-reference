# Remove Currency with LimoExpress

Removes a currency from the LimoExpress organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/remove-currency`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Remove Currency](https://api.limoexpress.me/api/docs/v1#/Currencies/removeACurrency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_id` | body | `string` | yes | Identifier of the currency to remove from the organization. |
