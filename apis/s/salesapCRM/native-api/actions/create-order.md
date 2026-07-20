# Create Order with SalesapCRM

Creates an order in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Order](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for an order, including type, attributes, and optional relationships. |
