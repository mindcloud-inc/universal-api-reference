# Create Product with SalesapCRM

Creates a product in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Product](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for a product, including type, attributes, and optional relationships. |
