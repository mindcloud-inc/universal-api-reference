# Upsert Products (Bulk) with Catalog Machine

Creates or updates multiple products in Catalog Machine.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Upsert Products (Bulk)](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products` | body | `list<object>` | yes | Bulk products payload. Example: [{"Code":"CM-TEST-001","Name":"Codex Test Product 1"}] |
