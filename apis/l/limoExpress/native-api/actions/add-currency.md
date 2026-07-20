# Add Currency with LimoExpress

Adds a currency to the LimoExpress organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/add-currency`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Add Currency](https://api.limoexpress.me/api/docs/v1#/Currencies/addACurrency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_id` | body | `string` | yes | Identifier of the currency to add to the organization. |
